## 研发效率的思考
软件要随业务的增长健康长大。<br>
在一个团队人少的时候沟通成本比较低，工作效率很高，但当业务增长，人员增长到一定程度，沟通效率就会下降，人越多产出反而越少。
<br>这时就要思考如果对业务作架构拆分，对业务进行拆分，并更具当前人员情况，合理的分配权责，这样不同的团队并行的互不干扰的作不同的事情，最后把他们的工作成果组合起来，达到1+1>=2的效果。


#### 软件的开发生命周期：确定业务需求 > 编码 》测试》上线
* 传统企业的软件开发模式：以不信任软件工程师为基础，以避免开发工程师犯错为核心的开发模式，由于不信任开发工程师，因而所有的需求沟通都要有文档来传递；要求软件工程师严格按照文档编码实现，并建立庞大的测试团队，防止软件工程师犯错，因此开发流程往往非常复杂，开不完的回忆，写不完的文档，而结果往往达不到预期。进而导致更多的流程、更多的会议和更复杂的文档，恶性循环，参与者苦不堪言。因为软件工程师与业务人员是分离的。
* 而新兴的互联网企业，回选择信任工程师文化，软件工程师既要懂得软件技术还要熟悉相关的业务，二者合为一体，其实很多业务本身也是有技术创造的，这就是现在流行的“技术驱动业务”
互联网的特点，是产品要更具市场的反馈快速的调整，每周都有迭代，如果不能更具市场的反馈及时对产品作出调整很可能会造成用户的流失，就要求我们采用信任工程师的文化，工程师对业务也非常了解，这也需要对业务作拆分，让不同的团队专注自己的业务领域。


### 拆分：
* 软件开发团队的拆分：
要把不同业务部门的需求用软件实现，就需要建立不同开发团队：<br>
情况1:多个业务团队对应一个软件开发团队，这种情况很容易出现软件开发人员处理不同业务，进而导致对个业务需求，以省事或者重用为理由，全部整合在一个软件中，这样就导致不同业务都提出需求的时候，软件开发团队内部之间，会产生大量的互相依赖，干扰，扯皮，也会产生大量的会议，降低整个团队的效率，最终会导致软件之间的依赖错综复杂，软件上线都要靠运气了。<br>
情况2:一个业务团队对应一个软件开发团队：
这个方式要求个业务部门或者产品都有对立的开发团队配合，每个软件开发团队只对应一个一方面的业务，这样锁形成的软件边界很清楚，沟通也很高效，业务团队对应的开发团队能够形成合力，软件工程师对自己领域的业务也更容易理解，更专注与如何通过技术对现有的业务改进，从而达到技术驱动业务，而不是被动的满足业务需求。

* 软件模块的拆分：
软件是软件团队的产物。当软件开发团队拆分时，对应的软件业也要拆分，否则
多个开发团队开发同一个软件：
这时候对代发的分支合并管理要求非常高，经常发生互相吧对方的代码冲掉的情况，导致生产事故，当软件需求较多，就会出现版本较多，版本之间互相干扰依赖，导致上线排队，拖慢产品交付。
软件拆分后一个软件开发团队开发一个软件，这样职责清晰，沟通简单高效。

```gantt
    title 项目开发流程
    section 项目确定
        需求分析       :a1, 2016-06-22, 3d
        可行性报告     :after a1, 5d
        概念验证       : 5d
    section 项目实施
        概要设计      :2016-07-05  , 5d
        详细设计      :2016-07-08, 10d
        编码          :2016-07-15, 10d
        测试          :2016-07-22, 5d
    section 发布验收
        发布: 2d
        验收: 3d
```
