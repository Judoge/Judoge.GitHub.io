## 块神君Judoge的小黑屋

You can use the [editor on GitHub](https://github.com/Judoge/Judoge.GitHub.io/edit/main/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/Judoge/Judoge.GitHub.io/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.


###这是klpbbs的测速（doge）

<!DOCTYPE HTML>
<html lang="zh-cn">
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <meta name="keywords" content="CPS测试,点击速度测试,手速测试,免费测试">
    <meta name="description" content="CPS测试,点击速度测试,手速测试,免费测试">
    <title>CPS测试</title>
    <link
    rel="stylesheet"
    href="https://cdn.jsdelivr.net/npm/mdui@1.0.1/dist/css/mdui.min.css"
    integrity="sha384-cLRrMq39HOZdvE0j6yBojO4+1PrHfB7a9l5qLcmRm/fiWXYY+CndJPmyu5FV/9Tw"
    crossorigin="anonymous"
    />
</head>
<body class="mdui-theme-primary-indigo mdui-theme-accent-blue mdui-theme-layout-auto">
    <div class="mdui-container">
        <br>
        <center>
            <div class="mdui-chip">
                <span class="mdui-text-center mdui-chip-title">这是一个CPS测试网页</span>
            </div>
            <div class="mdui-card mdui-m-t-1" style="width: 60%;min-width: 300px;">
                <div class="mdui-card-content">tips:点击按钮就开始测试了！</div>
                    <div id="match" style="display: block;">
                        剩余时间：<span id="time">10</span>s 点击次数：<span id="times">0</span>次
                        <div class="mdui-col mdui-p-l-2 mdui-m-t-1 mdui-p-r-2 mdui-m-b-4" style="max-width: 500px;">
                            <button id="start" onclick="start()" class="mdui-btn mdui-btn-raised mdui-btn-block mdui-color-theme-accent" style="height: 100px;"><h1>开始</h1></button>
                        </div>
                    </div>
                    <div id="match1" style="display:none">
                        <h3>测试结束</h3>
                        <h4>您的CPS为：<span id="match2">Null</span></h4>
                        <br>
                        <h4>该成绩为10秒平均点击速率。</h4>
                            <button onclick="document.getElementById('match1').style.display='none';document.getElementById('match').style.display='block';document.getElementById('times').innerHTML = 0;jc = 0;" class="mdui-btn mdui-btn-raised mdui-color-theme-accent mdui-m-b-2">重新测试</button>
                    </div>
                    <br>
                    Powered By KlpBBS
                    <div class="mdui-panel mdui-panel-gapless mdui-m-t-1" mdui-panel>
                        <div class="mdui-panel-item">
                            <div class="mdui-panel-item-header">更多操作选项
                                <i class="mdui-panel-item-arrow mdui-icon material-icons">keyboard_arrow_down</i>
                            </div>
                            <div class="mdui-panel-item-body">
                                <div class="mdui-btn-group mdui-m-t-1">
                                    <a href="javascript:history.back();"><button class="mdui-btn mdui-btn-raised mdui-ripple mdui-color-theme-accent">返回前页</button></a>
                                    <a href="/"><button class="mdui-m-l-1 mdui-btn mdui-btn-raised mdui-ripple mdui-color-theme-accent">返回首页</button></a>
                                </div>
                                <div class="mdui-btn-group mdui-m-t-1">
                                    <button class="mdui-btn mdui-btn-raised mdui-ripple mdui-color-theme-accent" mdui-dialog="{target: '#aboutPages'}">关于本页</button>
                                </div>
                            </div>
                        </div>
                    </div>
        </center>
        <div class="mdui-dialog" id="aboutPages">
            <div class="mdui-dialog-title">关于 About</div>
            <div class="mdui-dialog-content">本页面由 @苦力怕纸 开发<br>框架使用开源项目：MDUI<br>本页仓库：<a href="https://github.com/klpbbs/CPS-Test" target="_black">CPS-Test</a><br>苦力怕论坛，有你更精彩~</div>
            <div class="mdui-dialog-actions">
                <button class="mdui-btn mdui-ripple" mdui-dialog-close>关闭 Off</button>
            </div>
        </div>
    </div>
    <script>
        var jc = 0
        function start(){
            var times =document.getElementById('times');
            if (jc == 0){
                id = window.setInterval("time()",1000);
                document.getElementById('start').innerHTML = "<h1>点我</h1>";
            }
            if (document.getElementById("time").innerHTML != "No time"){
                jc = jc + 1;
                times.innerHTML = jc;
            }else{
            }
        }
        

        function time(){
            var time = document.getElementById("time");
            if (time.innerHTML == 0){
                time.innerHTML = "No time" ;
                document.getElementById('match').style.display="none";
                document.getElementById('match1').style.display="block";
                var times = document.getElementById('times').innerHTML;
                document.getElementById('match2').innerHTML = times / 10;
                clearInterval(id);
            }else{
                time.innerHTML = time.innerHTML-1;
            }
            if (time.innerHTML == 5){
                document.getElementById('start').innerHTML = "<h1>还有5秒！</h1>";
            }
            if(time.innerHTML == 3){
                document.getElementById('start').innerHTML = "<h1>还有3秒！</h1>";
            }
            if(time.innerHTML == 2){
                document.getElementById('start').innerHTML = "<h1>还有2秒！</h1>";
            }
            if(time.innerHTML == 1){
                document.getElementById('start').innerHTML = "<h1>还有1秒！</h1>";
            }
            if(time.innerHTML == 0){
                document.getElementById('start').innerHTML = "<h1>快！</h1>";
            }
            if(time.innerHTML == "No time"){
                document.getElementById('start').innerHTML = "<h1>开始！</h1>";
                time.innerHTML = 10 ;
            }
            if(time.innerHTML == 4){
                document.getElementById('start').innerHTML = "<h1>加油！</h1>"; 
            }
        }
    </script>
    <script
    src="https://cdn.jsdelivr.net/npm/mdui@1.0.1/dist/js/mdui.min.js"
    integrity="sha384-gCMZcshYKOGRX9r6wbDrvF+TcCCswSHFucUzUPwka+Gr+uHgjlYvkABr95TCOz3A"
    crossorigin="anonymous"
    ></script>
</body>
</html>
