# Protobuf

Protobuf是一种二进制数据格式，相比于传统的JSON格式体积更小。Protobuf依赖Proto文件进行编码和解码，没有Proto文件的情况下，可以在 `Raw` 标签下查看到不完整的数据。

![](arts/protobuf_01.png)

如果有Proto文件，配置后便可以查看完整的数据（以JSON的形式显示），在 `Protobuf` 标签下点击即可进入配置页面。

![](arts/protobuf_02.png)

另外，还可以通过 `工具` 菜单中的 `Protobuf` 选项进入配置列表。

Reqable需要通过请求URL来关联到Proto定义，因此需要输入完整的URL地址，必要时可以使用通配符 `*` 和 `?`。

Proto支持下面两种定义方式：

#### 本地文件

导入设备本地Proto文件。如果有多个依赖的Proto文件，请选择根Proto文件。

![](arts/protobuf_03.png)

#### 规范文件（推荐）

规范文件是指由Reqable管理的Proto文件，在下拉框中可以选择已有规范文件或者新建一个规范文件。如果有多个依赖的Proto文件，请选择根Proto文件。

![](arts/protobuf_04.png)

规范文件可以在Reqable中进行编辑，如果启用了云端数据同步功能，还可以保存到服务器以及实时同步更新到其他设备。

![](arts/protobuf_05.png)

请求和响应消息至少需要配置一个。

Proto配置完成后，便可以查看到解析后的protobuf消息了。

![](arts/protobuf_06.png)
