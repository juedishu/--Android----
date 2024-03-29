# 关于Android中台建设

### 背景介绍
  说到中台，不得不提Supercell这个公司，这是一家位于芬兰赫尔辛基的移动游戏公司，号称世界上最成功的移动游戏公司，2016年6月，腾讯以86亿美元收购了它84.3%的股权，员工总数不超过200人，人均贡献估值超过3.54亿人民币。它的特殊之处就在于，以2个或者5个，最多不超过7个员工组成的小团队进行游戏开发，团队需要的开发框架、工具和平台由一个独立部门提供，团队只需要专注于做什么样的产品，然后以最快的时间推出公测版，去C端用户市场进行检验，如果增长不及预期，则迅速放弃此产品，再进行新的尝试。说到这里可能有人会问，实验成功了自然功成名就，要是失败了呢？失败了，公司不但不会惩罚，相反还会开香槟庆祝，庆祝从失败中学到的经验教训。

### 为什么要用中台？
  由于企业后台往往并不能很好的支撑前台快速创新响应用户的需求，后台更多的是在解决企业管理效率问题，而中台要解决的才是前台的创新问题；大多数企业已有的后台，要么前台根本就用不，要么不好用，要么变更速度跟不上前台的节奏。而且系统创建之初，是为了实现后端资源的电子化管理，解决企业的效率问题，定制化困难。各个方面受限难以快速变化，以支持前台快速变化的创新需求。

### 大企业的步伐？
华为：“让平台炮火支撑精兵作战”；  
阿里：由“共享事业部”->“中台战略”，集合整个集团的运营、产品、技术能力；

### Android客户端的实现？
  说到它，不得不说移动互联网，移动互联网时代，如果用一个字来形容那就是：快。天下武功唯快不破，今天A厂出了这个功能，明天B厂就能做出来，大家就在比谁快，只有快才能获得用户，赢取流量。反映到客户端上面就是：快速推出新功能，通过数据分析找到后续优化点，再迅速迭代升级。著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。面对瞬息万变的外部环境，当然试错成本越低越好，必须先发制人。那么环境一样的话，就可以采用相同的作战策略，如何构筑客户端的中台呢？

  1.充分理解业务场景，在理解的基础之上加以合理的架构和拆分；
  2.降低业务层的纵深，将业务层圈定在ui及交互相关易变的部分；
  3.打破业务竖井，将不同业务之间共同的部分，稳定的部分抽取出来，封装成独立的服务提供给业务层使用，形成客户端的中台；

  例如现在开发的项目，我们将分享服务，上传服务，地图服务，热更新，上报等等诸多模块全部按子功能封装，放到共享版本库，当要使用时，直接从共享版本库中取出即可。下次开发中，只需要根据项目的子功能模块，取出即用即可；这样即确保了最小的变动，最大的提高了效率，同时保持了架构的稳定；

### 中台是一种方法
  总而言之，中台是一种思想理念，是一种面对剧烈变化的外部环境的，最小化成本策略，一种作战方式，一种方法论。它就是要给我们卸包袱，轻装上阵，快速变换进攻方向，机动灵活。中台不仅仅适用于宏观方面，组织机构调整、战略调整，也适用于一个像移动客户端这样的产品的技术架构演进，技术架构不是空中楼阁，是贯彻落实公司战略的必要条件，架构必须紧跟人员组织形式、公司市场策略，否则就是拖后腿，就是绊脚石。




