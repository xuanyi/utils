## 修改webkit滚动条样式

```
::-webkit-scrollbar {
    width: 6px;
    height: 6px;
}
::-webkit-scrollbar-track-piece{
    -webkit-border-radius: 6px;
}
::-webkit-scrollbar-thumb:vertical{
    height: 5px;
    background-color: #999999;
    -webkit-border-radius: 6px;
}
::-webkit-scrollbar-thumb:horizontal{
    width: 5px;
    background-color: #dfe1e0;
    -webkit-border-radius: 6px;
}
::-webkit-scrollbar-thumb:hover{
    background-color: #666;
}
```
