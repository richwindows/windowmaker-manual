
<details>
<summary><font size="+3">在下料之前我们需要先安排好路线和要求的时间</font></summary>

<font size="+2">我们可以在order中看到时间，可以根据时间排序</font>

![order-time](./images/routedate1.gif)  

![order-time](./images/routedate2.gif)

</details>

<br>

<details>
<summary><font size="+3">创建delivery batch</font></summary>

<font size="+2">只是创建好，而不schedule,我们在下料的batch中schedule的时候单子会自动进入这个delivery batch</font>

</details>

<br>

<details>
<summary><font size="+3">创建production batch, schedule it</font></summary>

<font size="+2">成功的话可以看到delivery batch number，路线和时间</font>

<font size="+2">失败的话，可能delivery batch没有创建，order没有设置routes和require date</font>

<font size="+2">当一个order中有门有窗，需要两种batch同时存在，否则schedule failed</font>

![schedule-failed](./images/create%20production%20batch.gif)
</details>

<br>

<details>
<summary><font size="+3">开始下料,每次都需要点击subbatch和process(先subbatch),这是一个处理数据的过程,结束后在DCA文件夹中会有各种batch的切割数据,需要转成天宜的格式</font></summary>

![subbatch](./images/subbatch.gif)

![process](./images/process.gif)
</details>

<br>

<details>
<summary><font size="+3">generate production document我们需要几个转成excel格式的下料单</font></summary>

![generate-production-document](./images/generate%20production.gif)
</details>

<br>

<details>
<summary><font size="+3">怎么查看一个batch是否下料,通过判断"√"</font></summary>

<font size="+2">finalise的就代表完成下料

如果有报告不能生成，我们需要unfinalize,再进行一遍subbatch,process</font>

![check-batch](./images/process.gif)
</details>

<br>

<details>
<summary><font size="+3">create door batch</font></summary>

<font size="+2">如果一个order里有门有窗，如果你拖动到window batch，那么它就会把order里的window放到那个window batch中， 门会找当日或临近的 door batch自动放进去, 如果没有door batch的话，会schedule failed</font>

![create-door-batch](./images/create%20door%20batch.gif)

</details>

<br>

<details>
<summary><font size="+3">batch中取消某个单子</font></summary>

<font size="+2" color="red">不选择删除，reschedule按钮不能用</font>

![cancel-order](./images/delete%20order%20from%20batch.gif)

</details>

<br>

<details>
<summary><font size="+3">move order to another batch</font></summary>

<font size="+2">两种方法</font>

![move-order](./images/moveorder1.gif)

![move-order-2](./images/moveorder2.gif)

</details>

<br>

<details>
<summary><font size="+3">batch中的单子需要unschedule之后才能修改required date和delivery route</font></summary>

<font size="+2" color="red">显示的是unschele,说明order是schedule的， 此状态不能修改数据，会出现问题</font>

![unschedule](./images/unschedulegif.gif)

</details>

<br>

<details>
<summary><font size="+3">一个完整的schedule,包schedule delivery,再Schedule production</font></summary>

![schedule-delivery](./images/whole%20schedule.gif)

</details>

<br>

<details>
<summary><font size="+3">结束后记得change status,便于分类</font></summary>

![schedule-delivery](./images/change%20status%20after%20shcdeule.gif)
</details>
