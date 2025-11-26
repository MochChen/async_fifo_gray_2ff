# async_fifo_gray_2ff
极简实现的异步FIFO（炫技），可以方便参考学习，FIFO介绍在这里：【verilog 异步fifo设计介绍】 https://www.bilibili.com/video/BV1dGjAzfE1a/?share_source=copy_web&amp;vd_source=0bac3deeee87254d962a2490c70512a5


# Async FIFO with Gray Code + 2-FF Synchronizer
- 深度 16（可参数化），无任何参考代码
- Gray 码指针 + 经典两级同步
- full = { ~rd_ptr_sync[4:3], rd_ptr_sync[2:0] } 
- 单向异步复位同步释放（仅 rd_rst_n 一路复位）
- 综合后 < 50 LUT，跨时钟域 300MHz+ 实测零亚稳（AI计算的）

作者：某小小专科菜鸟
