# SoftwareReuseDiscuss
##用户登录后始终在线，考虑低带宽、不稳定网络。
------------------
- **长连接心跳机制**:
- **消息不遗漏**:
- **消息不重复**:
- **消息压缩**:

##长连接心跳机制
  - **出现原因** ：在使用长连接的前提条件下，为确认客户端是处于连接状态还是断开的状态。常见应用是app的推送的服务。
  - **机制原理** : 维护一个长连接都需要心跳机制。心跳机制便是客户端发送一个心跳给服务器，服务器给客户端一个心跳应答，这样就形成客户端服务器的一次完整的握手，这个握手是让双方都知道他们之间的连接是没有断开，客户端是在线的。如果超过一个时间的阈值，客户端没有收到服务器的应答，或者服务器没有收到客户端的心跳，那么对客户端来说则断开与服务器的连接重新建立一个连接，对服务器来说只要断开这个连接即可。
  - **TCP keepalive** : [RFC1122#TCP Keep-Alives](https://tools.ietf.org/html/rfc1122#page-101)

--------------------------
#####`4月10日`前提交到Github上
