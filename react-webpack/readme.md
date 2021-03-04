# webapck + react 搭建

1. webpack基础搭建

2. 针对jsx进行loader配置
    > npm i @babel/preset-react -D 并且在.babelrc中引入
    ```ASN.1
    "presets": ["@babel/preset-env", "@babel/preset-react"],
    ```

3. 此处使用的垫片填充没有用@bable-polyfill, 而使用的@babel/plugin-transform-runtime，就不会污染全局。
    > npm i @babel/plugin-transform-runtime -D;  npm i @babel/runtime-corejs3 -S
    ```ASN.1
    "plugins": [
        [
            "@babel/plugin-transform-runtime",
            {
                // 配置corejs为3，需要预先安装@babel/runtime-corejs3
                // 配置corejs为2，需要预先安装@babel/runtime-corejs2
                // 配置corejs为false，需要预先安装@babel/runtime
                "corejs": 3
            }
        ]
    ]
    ```
