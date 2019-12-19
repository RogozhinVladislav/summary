## Antd

#### Изменить текст пустого поиска

```javascript
import { TreeSelect, Icon, ConfigProvider } from "antd";
...
const customizeRenderEmpty = () => (
    <div style={{ textAlign: 'center' }}>
        <Icon type="stop" style={{ fontSize: 20 }} />
        <p>Нет данных</p>
    </div>
);
...
<ConfigProvider renderEmpty={customizeRenderEmpty}>
    <TreeSelect
        ...
        showSearch
        treeNodeFilterProp="title"
        searchPlaceholder={"Поиск..."}
    >
        {this.renderTreeNode(data)}
    </TreeSelect>
</ConfigProvider>
...
```
