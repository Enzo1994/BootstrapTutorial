## 表单
##### 启动bootstrap表单：
```
<form class="form-inline">
    <div class="form-group form-group-lg has-success has-feedback" role="input">
        <span class="input-group-addon">@</span>
        <label for="exampleInputEmail1">Email address</label>
        <input type="email" class="form-control" id="exampleInputEmail1" placeholder="Email">
        <span class="glyphicon glyphicon-warning-sign form-control-feedback" ></span>
        <span class="glyphicon glyphicon-ok form-control-feedback"></span>
        <span class="glyphicon glyphicon-remove form-control-feedback" aria-hidden="true"></span>

    </div>
</form>
```
- 每个控件（label+控件）包裹在.form-group内
- 所有设置了 .form-control 类的 `<input>`、`<textarea>` 和 `<select>` 元素都将被默认设置宽度属性为 width: 100%;
- 输入栏头尾可以添加自定义内容`span.input-group-addon`
- div设置输入框变色警告：`.has-warning`、`.has-error`或`.has-success` ， *输入框结尾要配置span标签* 
- 使用.has-feedback给变色警告加图片
- div标签的role属性可设置button、input等

##### fieldset禁用：
- `<fieldset disable>`会禁用被包裹内的所有控件  
    * *注意：a标签链接不受影响，请使用js禁用*

##### 表单布局：
- 水平排列宽度百分百：`<form class="form-horizontal">`

- 内联排列：```<form class="form-inline">```
    - 只适用于视口（viewport）至少在 768px 宽度时（视口宽度再小的话就会使表单折叠）。
    - 输入框和单选/多选框控件默认被设置为 width: 100%;而在内联表单，我们将这些元素的宽度设置为 width: auto，因此，多个控件可以排列在同一行。

##### label的设置：
- ==label必须设置==
- 可以通过为 label 设置 ```.sr-only``` 类将其隐藏。
- 多选单选的label设置：
```html
<label class="checkbox-inline">
  <input type="checkbox" id="inlineCheckbox1" value="option1"> 1
</label>
```
- label标签有aria-label属性和aria-labelledby属性
```html
<div class="checkbox">
  <label>
    <input type="checkbox" id="blankCheckbox" value="option1" aria-label="...">
  </label>
</div>
```

##### 控件：
- 静态控件：如果需要在表单中将一行纯文本按控件布局位置和 label 元素放置于同一行，为 ```<p>``` 元素添加```.form-control-static```类即可。
```html
  <div class="form-group">
    <label class="col-sm-2 control-label">Email</label>
    <div class="col-sm-10">
      <p class="form-control-static">email@example.com</p>
    </div>
  </div>
```
- readonly只读
- 宽高：`<input class="form-control input-lg" type="text" placeholder=".input-lg">`
    - form-group-lg -控件和label
    - input-lg -控件
    - col-xs-2 -带有此类的div包裹一下控件