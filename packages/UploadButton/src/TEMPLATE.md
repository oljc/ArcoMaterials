%%API(index.vue)%%

### `按钮Props`

| 参数名 |    描述    |    类型     | 默认值 |
| ------| :--------: | :---------: | -----: |
| type  | 按钮的形状 | `square`、 `round` | `round`|
| size  | 按钮的大小 | `mini`、 `small` 、`medium`、`large`| `medium`|


### `事件Events`

| 事件名 |    描述    |  参数 |
| ------ | :----------: | :------: | 
| click  | 点击按钮时触发 | event:`Event` |

按钮处于loading、success状态时，按钮会处于禁止点击状态。防止触发点击事件。
## Demos

%%MATERIAL(demo/index.ts)%%