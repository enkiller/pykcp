# pykcp

基于skywind3000/kcp 实现的 Python 版本。

- [skywind3000/KCP](https://github.com/skywind3000/kcp)

## 使用示例

python >= 3.7

```python
from pykcp import Kcp

# 继承 Kcp 对象，实现 output 方法
class MyKcp(Kcp):
    def output(self, buf):
        pass
```

## API 对应表

| C 版本 | Python 版本 |
| ------ | ----------- |
| ikcp_create | Kcp() |
| ikcp_release |  |
| ikcp_setoutput | 继承 Kcp 对象，覆盖 output 方法 |
| ikcp_recv | Kcp.recv() |
| ikcp_send | Kcp.send |
| ikcp_update | Kcp.update |
| ikcp_check | Kcp.check |
| ikcp_input | Kcp.input |
| ikcp_flush | Kcp.flush |
| ikcp_peeksize | Kcp.peeksize |
| ikcp_setmtu | Kcp.setmtu |
| ikcp_wndsize | Kcp.wndsize |
| ikcp_waitsnd | Kcp.waitsnd |
| ikcp_nodelay | Kcp.nodelay |
| ikcp_getconv | Kcp.getconv |
