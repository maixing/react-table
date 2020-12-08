- ### 安装screenv-table

  ```js
  npm install screenv-table -save
  ```

- [预览](http://www.screenv.com/reacttable/index.html#/home/table)

- ### 使用

  ```js
  import {SelectTable} from "screenv-table";
  import 'screenv-table/dist/index.css';
  <SelectTable
  	columns={columns}
  	data={this.state.data}
  	menus={menus}
  	events={{
          onClickEvent: (evt, data, type) => {
              console.log('ScTable onClickEvent---->>%o,%o,%o', evt, data, type);
          },
  	}}>
  </SelectTable>
  ```
  
- ### 属性说明

  ```js
  menus //右键列表数据，格式为[{id:'',name:''}]
  /**
  * events 对象属性
  * {
  *  	onClickEvent:function,//(evt, record, 'onClick|onDoubleClick')
  *	onMouseEvent:function,//(evt, record, 'onMouseEnter|onMouseLeave')
  *	onSelectEvent:function,//(evt, record, 'onSelectEvent')
  *	onMenuEvent:function//(evt, data)
  * }
  */
  events:Object
  staticLabel //左上角展示文字 默认是活动告警
  ```
  

  
- ### 数据项说明

  - columns

    ```js
    let columns = [
        {
            code: 'key',//数据项key
            title: 'title',//表头中文字段
            width: 100,//宽度设置,
            render: null,//react组件，渲染器
            features: { sortable: true },//sortable 是否显示排序
        }
    ]
    ```
    
  - alarmLevels
  
    ```js
  alarmLevels: {
      level1: {
        label: '一级告警',
  	  value: '1',
  	  color: '#ff6464'
      },
      level2: {
        label: '二级告警',
  	  value: '2',
  	  color: '#ffa85a'
      },
      level3: {
        label: '三级告警',
  	  value: '3',
  	  color: '#ffec6f'
      },
      level4: {
        label: '四级告警',
  	  value: '4',
  	  color: '#8bbcfe'
      },
      level5: {
        label: '五级告警',
  	  value: '5',
  	  color: '#8bbddd'
      },
    },
    ```
  
  - filters
  
    ```js
    let filters = [
        {
            name: '告警级别',
            field: 'severity',
            items: [
              {
                value: '1',
                name: '一级告警',
              },
              {
                value: '2',
                name: '二级告警',
              },
              {
                value: '3',
                name: '三级告警',
              },
              {
                value: '4',
                name: '四级告警',
              },
            ],
      	},
        {
            name: '专业',
            field: 'domain',
            items: [
              {
                value: '核心网',
                name: '核心网',
              },
              {
                value: '数据网',
                name: '数据网',
              },
              {
                value: '传送网',
                name: '传送网',
              },
              {
                value: '动环网',
                name: '动环网',
              },
            ],
        },
    ]
    ```
  
    
  


