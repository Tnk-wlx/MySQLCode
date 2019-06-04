##### 全国省市区划表

~~~sql
-- Create table
create table PM_APP_QUHUA
(
  id           number not null,
  citycode     varchar2(10) default ' ',
  provincecode varchar2(10) default ' '
)
tablespace SHINEYUE40
  pctfree 10
  initrans 1
  maxtrans 255
  storage
  (
    initial 64K
    next 1M
    minextents 1
    maxextents unlimited
  );
-- Add comments to the table 
comment on table PM_APP_QUHUA
  is '全国省市区划表';
-- Add comments to the columns 
comment on column PM_APP_QUHUA.id
  is '记录唯一id';
comment on column PM_APP_QUHUA.citycode
  is '市级区划代码';
comment on column PM_APP_QUHUA.provincecode
  is '省级区划代码(北京市等直辖市属于省级)';

~~~
