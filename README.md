# 构建环境

- npm 6.5.0
- node 10.15.0
- webpack 1.13.2

# 清理NPM模块的目录
```
rm -rf node_modules
```

# 安装NPM模块
```
cnpm install 
```

# 记得备份，清理
```
rm -rf source/*
```

# 开发可以执行以下命令，此时会用webpack打包，并把文件编译到source目录下，但编译后的文件不会经过压缩处理
# 由于webpack打包完成后，不会自动退出，当看到以下日志信息，则代表编译成功，可以使用快捷键 Crtl + C 强制退出
```
npm run dev
```
