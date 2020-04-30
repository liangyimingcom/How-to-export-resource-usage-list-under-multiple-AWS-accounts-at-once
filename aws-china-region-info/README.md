# AWS中国区域信息
AWS区域信息记录
 <br>


# AWS中国区域传输费用图解
<br>
在AWS中国宁夏区在网络传输中可能产生的费用梳理
<br>更新时间: 2019/08/02



# 免责说明
<br>此价格是2019年8月2日截至的费用，仅供参考
<br>更多的费用详情还请参考具体的账单
<br>当您对方案需要进一步的沟通和反馈后，可以联系 nwcd_labs@nwcdcloud.cn 获得更进一步的支持。
<br>如果有更多的内容，欢迎在 github 项目issue中留言反馈bugs。

# 项目说明


# 在AWS宁夏区域传输费用图解 明细
<img src="https://github.com/nwcdlabs/aws-region-info/blob/master/%E4%B8%AD%E5%9B%BD%E5%8C%BA%E5%9F%9F%E4%BC%A0%E8%BE%93%E8%B4%B9%E7%94%A8%E5%9B%BE%E8%A7%A320190802.png" />
# 在中国区域CDN费用组成总结
<img src="https://github.com/nwcdlabs/aws-region-info/blob/master/CDN%E8%B4%B9%E7%94%A8%E7%BB%84%E6%88%90%E6%80%BB%E7%BB%93.png" />

# 总结：
 <br>1，传入费用不收费 
 <br>2，所有出站就是从AWS服务到Internet的费用：直接或者VPN到公网) ¥0.93/GB;经过CloudFront到公网¥ 0.30866/GB;经过DX到公网 ¥ 0.28/GB;
 <br>3，区域间传输有费用 ¥0.6003/GB
 <br>4，一个region的不同VPC之间有费用¥0.067/GB;不同可用区间公有子网或者私有子网之间的传输有费用¥0.067/GB;同一个子网内使用公网IP或者弹性IP传入传出都有费用¥0.067/GB;
 <br>5，专有线路传出有费用¥0.28/GB，另外有端口使用费



# 参考
<br>https://www.amazonaws.cn/directconnect/pricing/
<br>https://www.amazonaws.cn/ec2/pricing/
<br>https://www.amazonaws.cn/en/cloudfront/pricing/
