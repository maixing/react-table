- ### 安装react-table

  ```js
  npm install screenv-table -save
  ```

- [Demo](http://www.screenv.com/reacttable/index.html#/home/table)

- ### 使用

  ```js
  import {SelectTable} from "screenv-table";
  import 'react-table/dist/index.css';
  <SelectTable columns={columns} data={data} menus={menus}></SelectTable>
  ```
  
- ### 属性说明

  ```js
  expandKey  #树结构展开key字段，默认是alarmTitle
  
  menus #右键列表数据，格式为[{id:'',name:''}]
  
  onClickEvent # 鼠标点击和双击事件 (evt,type) type:onClick||onDoubleClick
  
  onMouseEvent: # 鼠标enter,Leave事件，默认为(evt,type) type:onMouseEnter||onMouseLeave
  
  onSelectEvent: # 多选框选择事件 (selects) 行数据集合
  
  onMenuEvent # 右键事件(evt,data) data:右键数据项
  
  staticLabel #左上角展示文字 默认是活动告警
  ```

  

- ### 数据项说明

  - columns

    ```js
    let columns = [
        {
            key: 'key',//数据项key
            dataKey: 'key',//数据项key
            title: 'title',//表头中文字段
            width: 100,//宽度设置,
            cellRenderer: Element,//react组件，渲染器
            resizable:true||false,//是否列可拖拽,
            frozen: 'left'||'right'||true||false
        }
    ]
    ```
  
  
  


