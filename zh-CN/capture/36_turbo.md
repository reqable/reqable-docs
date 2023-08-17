# 极速模式

Reqable提供了极速模式，用来优化频繁UI更新带来的性能问题。在极速模式下，调试列表的UI不会更新，但是[网关](gateway)、[镜像](mirror)、[脚本](script)、[重写](rewrite)和[断点](breakpoint)功能仍然生效。此模式有助于Reqable一直保持较低的系统资源占用，同时保证其他扩展功能的正常运行。

![](arts/turbo_01.png)