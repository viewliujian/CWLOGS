>**2018/07/19**

    1.Y6  62262修改拆分付款金额
    付款申请单号：R04FKSQ20180600104
>**2018/8/7**
```sql
1.select * from db.tbavbx040 t  where t.custno='1300056'and t.compid='R04'and t.avno='AV2018080300003';  
  新增prodtype字段HRCA、prodclass=‘H’
  鲁西工业只有一笔贴息单开的，确认收入显示失败，提示
 
2.付款申请单已发送稽核查收不到
  查询付款状态，流程
  select * from db.tbapcheckrec t where t.payapplyno like 'R01FKSQ20180800156';
  查询CHECKEMP 是否为汉字，可能在录入付款单时输入的是汉字
  select * from db.tbappayapply  t where t.payapplyno like 'R01FKSQ20180800156';
  上述两个地方汉字修改为工号即可
3.蒙阴流程修改
  select * from Db.tbappayapply t where t.payapplyno='R14FKSQ20180800007';
  select * from  Db.tbapcheckrec t where t.payapplyno='R14FKSQ20180800007';
  select * from db.tbapchecklevel t where t.deptno like '%Q261%';
4.SELECT * FROM DB.TBarbx03 where CUSTNO='4100030'and compid='R03'
  修改产品大类为S
```
