# @vue/cli-plugin-unit-jest

[英文原版](https://github.com/vuejs/vue-cli/tree/dev/packages/\@vue/cli-plugin-unit-jest/README.md)

> vue-cli 的 unit-jest 插件

## 注入的命令

- **`vue-cli-service test:unit`**

通过 Jest 运行单元测试。默认的 `testMatch` 是 `<rootDir>/(tests/unit/**/*.spec.(js|jsx|ts|tsx)|**/__tests__/*.(js|jsx|ts|tsx))`，它匹配：

  - 任何 `tests/unit` 中以 `.spec.(js|jsx|ts|tsx)` 结尾的文件；
  - 任何 `__tests__` 目录中的 js(x)/ts(x) 文件。

  使用：`vue-cli-service test:unit [options] <regexForTestFiles>`

  支持所有的 [Jest 命令行选项](https://facebook.github.io/jest/docs/en/cli.html)。

## 调试测试代码

注意直接运行 `jest` 会失败，因为 Babel preset 需要提示 (hint) 才能让代码在 Node.js 中运行，所以你必须通过 `vue-cli-service test:unit` 来运行测试代码。

如果你想要通过 Node inspector 调试你的测试代码，可以运行如下代码：

``` sh
# macOS or linux
node --inspect-brk ./node_modules/.bin/vue-cli-service test:unit

# Windows
node --inspect-brk ./node_modules/@vue/cli-service/bin/vue-cli-service.js test:unit
```

## 配置

Jest 可以通过你项目根目录中的 `jest.config.js` 文件或 `package.json` 文件中 `jest` 字段的进行配置。

## 在已创建的项目中安装

``` sh
vue add @vue/unit-jest
```
