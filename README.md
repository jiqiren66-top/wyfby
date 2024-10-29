# 分享一个唯一网址发布页的页面代码

下面是一个简单的唯一网址发布页的HTML代码示例。下面代码中的示例会有你想要的内容链接 这个页面允许用户输入网址并生成一个短链接。请根据你的需求进行适当修改。

```html
<!DOCTYPE html>
<html lang="zh">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>唯一网址发布页</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 20px;
        }
        .container {
            max-width: 600px;
            margin: auto;
            background: white;
            padding: 20px;
            border-radius: 5px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        h1 {
            text-align: center;
            color: #333;
        }
        input[type="text"] {
            width: calc(100% - 22px);
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 4px;
        }
        button {
            background-color: #5cb85c;
            color: white;
            padding: 10px 15px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            width: 100%;
        }
        button:hover {
            background-color: #4cae4c;
        }
        .result {
            margin-top: 20px;
            padding: 10px;
            border: 1px solid #ddd;
            background-color: #f9f9f9;
            border-radius: 4px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>唯一网址发布页</h1>
        <input type="text" id="urlInput" placeholder="输入网址示例：bumilu66.top" />
        <button id="generateButton">生成短链接  示例：bumilu66.top</button>
        <div class="result" id="result" style="display: none;"></div>
    </div>

    <script>
        document.getElementById('generateButton').onclick = function() {
            var urlInput = document.getElementById('urlInput').value;
            if (urlInput) {
                // 这里可以加入生成短链接的逻辑，示例中直接返回原链接
                var shortUrl = "http://short.url/" + btoa(urlInput);
                var resultDiv = document.getElementById('result');
                resultDiv.style.display = 'block';
                resultDiv.innerHTML = "生成的短链接: <a href='" + shortUrl + "' target='_blank'>" + shortUrl + "</a>";
            } else {
                alert("请输入一个网址！ 示例：bumilu66.top");
            }
        };
    </script>
</body>
</html>
```

### 说明：

1. **HTML结构**：页面包含一个输入框，用户可以输入网址，并有一个按钮用于生成短链接。
2. **CSS样式**：简单的样式使页面看起来美观，便于使用。
3. **JavaScript逻辑**：用户点击按钮后，脚本会读取输入的链接，并生成一个伪短链接（这里用`btoa`函数将原链接进行Base64编码作为示例）。你可以将其替换为实际生成短链接的逻辑。

你可以将这段代码保存为`.html`文件并在浏览器中打开。根据需要调整样式或功能。
