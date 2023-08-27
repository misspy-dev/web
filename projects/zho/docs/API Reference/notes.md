# `misspy.Bot.notes`
## 注释
获取笔记列表。

名称 | 类型 | 默认 | 说明 |
| - | - | - | - |
| local | bool | False | 仅检索本地创建的笔记。<br> |
|reply | bool || 设置为“True”以仅获取回复，“False”以获取非回复。如果不设置该值，无论是否回复都会收到备注。<br> |
| renote | bool | | 设置为“True”以仅获取注释，设置为“False”以获取非注释。如果您未设置值，则无论是否是重新注释，您都会收到注释。|
| withFiles | bool | | 设置为“True”仅获取带附件的笔记，“False”仅获取不带附件的笔记。如果您不设置值，您将获得带有或不带有附件的注释。|
| poll | bool | | 设置为“True”以仅获取带有民意调查的笔记，“False”以仅获取没有民意调查的笔记。如果您不设置值，您将获得带有或不带有投票的注释。|
| limit | int | 10 | 指定要检索的最大注释数。|
|sinceId | str | | 如果指定，则返回 id 大于该值的注释。<br> |
| untilId | str | | 如果指定，则返回 id 小于该值的注释。<br> |

## 笔记_创建
创建笔记。回复和重记也是用这个功能完成的。

名称 | 类型 | 默认 | 说明 |
| - | - | - | - |
| 可见性 | str<br>(`public` `home` `followers` `specified`) | public | 注释的可见范围。|
|visibleUserIds |list<br>(str)||可以查看注释的用户 ID 列表。仅在指定可见性时适用。<br> |
text | str &#124; None | | 注释的正文。<br> |
| cw | str &#124; 无 | | 注释的 CW。|
| localOnly | bool | False | True 仅在本地发布。|
| noExtractMentions | bool | False | 如果为 true，则不从正文中提取提及内容。|
| noExtractHashtags | bool | False | True 不从正文中提取主题标签。|
| noExtractEmojis | bool | False | 如果为 true，则不从正文中提取表情符号。<br> |
| fileIds | list<br>(str) | | 要附加的文件的 ID。<br> |
|replyId|str&#124;无||要回复的注释的id。|
| renoteId | str &#124; None | | 要重新注释的注释的 id。|
| channelId | str &#124; None | | 要发布到的频道的 id。<br> |
| poll | object &#124; None | | 投票参数。|

### 类型

名称 | 类型 | 默认 | 说明 |
| - | - | - | - |
| 选择 | 列表 | ||
| multiple | bool | False | True 允许多项选择。<br> |
| expiresAt | int &#124;无 | | 投票截止日期。以纪元秒为单位指定。<br> |
| 过期后 | int &#124;如果指定了expiresAt，则expiresAt优先。<br> |

<!--
名称 | 类型 | 默认 | 说明 |
| - | - | - | - |
| | | | |
| | | | |
| | | | |
-->
## 注释_删除
删除注释。

名称 | 类型 | 默认 | 说明 |
| - | - | - | - |
| noteId | str | | 笔记的 id。|