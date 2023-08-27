# `misspy.Bot.notes`
## notes
Get a list of notes.

Name | Type | Default | Description |
| - | - | - | - |
| local | bool | False | Only retrieve locally created notes.<br> |
| reply | bool | | Set to `True` to get only replies, `False` to get non-replies.If you don't set the value, you will get the note regardless of whether it is a reply or not.<br> |
| renote | bool | | Set to `True` to get only renotes, `False` to get non-renotes.If you don't set a value, you get the note regardless of whether it's a renote or not.|
| withFiles | bool | | Set to `True` to get only notes with attachments, `False` to get only notes without attachments.If you don't set a value, you get notes with or without attachments.|
| poll | bool | | Set to `True` to get only notes with polls, `False` to get only notes without polls.If you don't set a value, you'll get notes with or without votes.|
| limit | int | 10 | Specifies the maximum number of notes to retrieve.|
|sinceId | str | | If specified, returns notes whose id is greater than that value.<br> |
| untilId | str | | If specified, returns notes whose id is less than that value.<br> |

## notes_create
Create notes.Reply and Renote are also done with this function.

Name | Type | Default | Description |
| - | - | - | - |
| visibility | str<br>(`public` `home` `followers` `specified`) | public | Visibility range of the note.|
| visibleUserIds | list<br>(str) | | List of user ids that can view the note.Applies only when visibility is specified.<br> |
text | str &#124; None | | The body of the note.<br> |
| cw | str &#124; None | | CW of the note.|
| localOnly | bool | False | True to post locally only.|
| noExtractMentions | bool | False | If true, do not extract mentions from the body.|
| noExtractHashtags | bool | False | True does not extract hashtags from the body.|
| noExtractEmojis | bool | False | If true, do not extract emojis from the body.<br> |
| fileIds | list<br>(str) | | The ids of the files to attach.<br> |
| replyId | str &#124; None | | The id of the note to reply to.|
| renoteId | str &#124; None | | The id of the note to renote.|
| channelId | str &#124; None | | The id of the channel to post to.<br> |
| poll | object &#124; None | | Parameters for voting.|

### types

Name | Type | Default | Description |
| - | - | - | - |
| choices | list | ||
| multiple | bool | False | True to allow multiple selections.<br> |
| expiresAt | int &#124; None | | Deadline for voting.Specified in epoch seconds.<br> |
| expiredAfter | int &#124;If specified with expiresAt, expiresAt takes precedence.<br> |

<!--
Name | Type | Default | Description |
| - | - | - | - |
| | | | |
| | | | |
| | | | |
-->
## notes_delete
Delete notes.

Name | Type | Default | Description |
| - | - | - | - |
| noteId | str | | The id of the note.|