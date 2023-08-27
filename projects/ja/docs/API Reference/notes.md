# `misspy.Bot.notes`
## notes
ノート一覧を取得します。

| Name | Type | Default | Description |
| - | - | - | - |
| local | bool | False | ローカルで作成されたノートのみを取得します。<br> |
| reply | bool |  | `True` にすると返信だけを、 `False` にすると返信以外を取得します。値を設定しなければ返信であるかそうでないかに関係なくノートを取得します。<br> |
| renote | bool |  | `True` にするとリノートだけを、 `False` にするとリノート以外を取得します。値を設定しなければリノートであるかそうでないかに関係なくノートを取得します。 |
| withFiles | bool |  | `True` にすると添付ファイルのあるノートだけを、 `False` にすると添付ファイルがないノートだけを取得します。値を設定しなければ添付ファイルの有無にかかわらずノートを取得します。 |
| poll | bool |  | `True` にすると投票を含むノートだけを、 `False` にすると含まないノートだけを取得します。値を設定しなければ投票の有無にかかわらずノートを取得します。 |
| limit | int | 10 | 取得するノートの最大数を指定します。 |
| sinceId | str |  | 指定すると、idがその値よりも大きいノートを返します。<br> |
| untilId | str |  | 指定すると、idがその値よりも小さいノートを返します。<br> |

## notes_create
ノートを作成します。返信やRenoteもこの関数で行います。

| Name | Type | Default | Description |
| - | - | - | - |
| visibility | str<br>(`public` `home` `followers` `specified`) | public | ノートの公開範囲。 |
| visibleUserIds | list<br>(str) |  | ノートを閲覧可能なユーザーのidのリスト。visibilityがspecifiedの場合のみ適用されます。<br> |
| text | str &#124; None |  | ノートの本文。<br> |
| cw | str &#124; None |  | ノートのCW。 |
| localOnly | bool | False | Trueにすると、ローカルのみに投稿されます。 |
| noExtractMentions | bool | False | Trueにすると、本文からメンションを展開しません。 |
| noExtractHashtags | bool | False | Trueにすると、本文からハッシュタグを展開しません。 |
| noExtractEmojis | bool | False | Trueにすると、本文から絵文字を展開しません。<br> |
| fileIds | list<br>(str) |  | 添付するファイルのid。<br> |
| replyId | str &#124; None |  | 返信先のノートのid。 |
| renoteId | str &#124; None |  | Renote対象のノートのid。 |
| channelId | str &#124; None |  | 投稿先のチャンネルのid。<br> |
| poll | object &#124; None |  | 投票に関するパラメータ。 |

### 型

| Name | Type | Default | Description |
| - | - | - | - |
| choices | list |  | 選択肢。 |
| multiple | bool | False | Trueにすると、複数選択を許容します。<br> |
| expiresAt | int &#124; None |  | 投票の締め切り。エポック秒で指定します。<br> |
| expiredAfter | int &#124; None |  | 指定すると、ノート作成からexpiredAfter秒後に投票を締め切ります。expiresAtと併せて指定した場合、expiresAtが優先されます。<br> |

<!--
| Name | Type | Default | Description |
| - | - | - | - |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
-->
## notes_delete
ノートを削除します。

| Name | Type | Default | Description |
| - | - | - | - |
| noteId | str |  | ノートのid。 |