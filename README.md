<!DOCTYPE html>
<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8"/>
    <title></title>
	<meta charset="utf-8" />
    <style>
        div{
            width:200px;
            height:200px;
            border:1px solid blue;
            display:none;
        }
    </style>
    <script>
        window.onload = function () {
            var inputs = document.querySelectorAll("input");
            var divs = document.querySelectorAll("div");
            console.log(inputs);
            console.log(divs);
            var last = inputs[0];
            for (var i = 0; i < inputs.length; i++) {
                inputs[i].index = i;
                inputs[i].onclick = function () {                    
                    last.style.background = '';
                    divs[last.index].style.display = 'none';                    
                    //this.style.background = 'yellow';
                    divs[this.index].style.display = 'block';
                    last = this;
                }
            }
        };
    </script>
</head>
<body>
    <input type="button" id="" value="选项1" />
    <input type="button" id="" value="选项2" />
    <input type="button" id="" value="选项3" />
    <div style="display:block">内容1</div>
    <div>内容2</div>
    <div>内容3</div>
</body>
</html>
