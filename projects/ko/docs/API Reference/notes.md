# `misspy.Bot.notes`
## notes
노트 목록을 가져옵니다.

| Name | Type | Default | Description |
| - | - | - | - |
| local | bool | False | 로컬로 작성된 노트 만 가져옵니다.<br> |
| reply | bool | | `True` 로 하면 회신만을, `False` 로 하면 회신 이외를 취득합니다.값을 설정하지 않으면 회신인지 아닌지에 관계없이 노트를 취득합니다.<br> |
| renote | bool | | `True` 로 하면 리노트만을, `False` 로 하면 리노트 이외를 취득합니다.값을 설정하지 않으면 리노트인지 그렇지 않은지에 관계없이 노트를 취득합니다.|
| withFiles | bool | | `True` 로 하면 첨부 파일이 있는 노트만을, `False` 로 하면 첨부 파일이 없는 노트만을 취득합니다.값을 설정하지 않으면 첨부 파일의 유무에 관계없이 노트를 취득합니다.|
| poll | bool | | `True` 로 하면 투표를 포함한 노트만을, `False` 로 하면 포함하지 않는 노트만을 취득합니다.값을 설정하지 않으면 투표의 유무에 관계없이 노트를 취득합니다.|
| limit | int | 10 | 검색할 노트의 최대 수를 지정합니다.|
| sinceId | str | | 지정하면, id가 그 값보다 큰 노트를 돌려줍니다.<br> |
| untilId | str | | 지정되면, id가 그 값보다 작은 노트를 리턴합니다.<br> |

## notes_create
노트를 만듭니다.회신이나 Renote도 이 함수로 합니다.

| Name | Type | Default | Description |
| - | - | - | - |
| visibility | str<br> (`public` `home` `followers` `specified`) | public | 노트의 공개 범위.|
| visibleUserIds | list<br>(str) | | 노트를 볼 수 있는 사용자의 ID 목록입니다.visibility가 specified인 경우에만 적용됩니다.<br> |
| text | str &#124; None | | 노트 본문.<br> |
| cw | str &#124; None | | 주 CW.|
|localOnly|bool|False|True로 설정하면 로컬에만 게시됩니다.|
|noExtractMentions|bool|False|True로 설정하면 본문에서 멘션을 확장하지 않습니다.|
|noExtractHashtags|bool|False|True로 설정하면 본문에서 해시태그를 확장하지 않습니다.|
|noExtractEmojis|bool|False|True로 설정하면 본문에서 이모티콘을 확장하지 않습니다.<br> |
| fileIds | list<br>(str) | | 첨부할 파일의 ID.<br> |
| replyId | str &#124; None | | 답장 노트 ID .|
|renoteId|str &#124;None||Renote 대상 노트의 id.|
| channelId | str &#124; None | | 게시할 채널의 ID입니다.<br> |
| poll | object &#124; None | | 투표에 대한 매개변수.|

### 유형

| Name | Type | Default | Description |
| - | - | - | - |
| choices | list | | 선택.|
|multiple|bool|False|True로 설정하면 다중 선택을 허용합니다.<br> |
| expiresAt | int &#124; None | | 투표 마감일.에포크초로 지정합니다.<br> |
| expiredAfter | int &#124; None | | 지정하면 노트 작성 후 expiredAfter 초 후에 투표를 마감합니다.expiresAt과 함께 지정하면 expiresAt이 우선합니다.<br> |

<!--
| Name | Type | Default | Description |
| - | - | - | - |
| | | | |
| | | | |
| | | | |
-->
## notes_delete
메모를 삭제합니다.

| Name | Type | Default | Description |
| - | - | - | - |
| noteId | str | | 노트 ID.|