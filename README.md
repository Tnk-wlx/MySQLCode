##### 全国省市区划表

~~~sql
-- Create table
create table PM_APP_SHENGQUHUA
(
  id            number not null,
  provincecode  varchar2(10) default ' ',
  pname         varchar2(20) default ' ',
  jiancheng     varchar2(6)  default ' '
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
comment on table PM_APP_SHENGQUHUA
  is '全国省区划表';
-- Add comments to the columns 
comment on column PM_APP_SHENGQUHUA.id
  is '记录唯一id';
comment on column PM_APP_SHENGQUHUA.provincecode
  is '省级区划代码(北京市等直辖市属于省级)';
comment on column PM_APP_SHENGQUHUA.pname
  is '区划名称';
comment on column PM_APP_SHENGQUHUA.jiancheng
  is '区划简称';

-- Create table
create table PM_APP_SHIQUHUA
(
  id            number not null,
  citycode      varchar2(10) default ' ',
  cname         varchar2(30) default ' ',
  provincecode   varchar2(10)  default ' '
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
comment on table PM_APP_SHIQUHUA
  is '全国市区划表';
-- Add comments to the columns 
comment on column PM_APP_SHIQUHUA.id
  is '记录唯一id';
comment on column PM_APP_SHIQUHUA.citycode
  is '市级区划代码';
comment on column PM_APP_SHIQUHUA.cname
  is '区划名称';
comment on column PM_APP_SHIQUHUA.provincecode
  is '所属省区划代码';
  
  
  -- 插入省区划表pm_app_shengquhua
insert into pm_app_shengquhua(id, provincecode, pname, jiancheng) values (f_newid, '110000', '北京市', '京');
insert into pm_app_shengquhua(id, provincecode, pname, jiancheng) values (f_newid, '120000', '天津市', '津');
insert into pm_app_shengquhua(id, provincecode, pname, jiancheng) values (f_newid, '130000', '河北省', '冀');
insert into pm_app_shengquhua(id, provincecode, pname, jiancheng) values (f_newid, '140000', '山西省', '晋');
insert into pm_app_shengquhua(id, provincecode, pname, jiancheng) values (f_newid, '150000', '内蒙古自治区', '蒙');
insert into pm_app_shengquhua(id, provincecode, pname, jiancheng) values (f_newid, '210000', '辽宁省', '辽');
insert into pm_app_shengquhua(id, provincecode, pname, jiancheng) values (f_newid, '220000', '吉林省', '吉');
insert into pm_app_shengquhua(id, provincecode, pname, jiancheng) values (f_newid, '230000', '黑龙江省', '黑');
insert into pm_app_shengquhua(id, provincecode, pname, jiancheng) values (f_newid, '310000', '上海市', '沪');
insert into pm_app_shengquhua(id, provincecode, pname, jiancheng) values (f_newid, '320000', '江苏省', '苏');
insert into pm_app_shengquhua(id, provincecode, pname, jiancheng) values (f_newid, '330000', '浙江省', '浙');
insert into pm_app_shengquhua(id, provincecode, pname, jiancheng) values (f_newid, '340000', '安徽省', '皖');
insert into pm_app_shengquhua(id, provincecode, pname, jiancheng) values (f_newid, '350000', '福建省', '闽');
insert into pm_app_shengquhua(id, provincecode, pname, jiancheng) values (f_newid, '360000', '江西省', '赣');
insert into pm_app_shengquhua(id, provincecode, pname, jiancheng) values (f_newid, '370000', '山东省', '鲁');
insert into pm_app_shengquhua(id, provincecode, pname, jiancheng) values (f_newid, '410000', '河南省', '豫');
insert into pm_app_shengquhua(id, provincecode, pname, jiancheng) values (f_newid, '420000', '湖北省', '鄂');
insert into pm_app_shengquhua(id, provincecode, pname, jiancheng) values (f_newid, '430000', '湖南省', '湘');
insert into pm_app_shengquhua(id, provincecode, pname, jiancheng) values (f_newid, '440000', '广东省', '粤');
insert into pm_app_shengquhua(id, provincecode, pname, jiancheng) values (f_newid, '450000', '广西壮族自治区', '桂');
insert into pm_app_shengquhua(id, provincecode, pname, jiancheng) values (f_newid, '460000', '海南省', '琼');
insert into pm_app_shengquhua(id, provincecode, pname, jiancheng) values (f_newid, '500000', '重庆市', '渝');
insert into pm_app_shengquhua(id, provincecode, pname, jiancheng) values (f_newid, '510000', '四川省', '川');
insert into pm_app_shengquhua(id, provincecode, pname, jiancheng) values (f_newid, '520000', '贵州省', '黔');
insert into pm_app_shengquhua(id, provincecode, pname, jiancheng) values (f_newid, '530000', '云南省', '滇');
insert into pm_app_shengquhua(id, provincecode, pname, jiancheng) values (f_newid, '540000', '西藏自治区', '藏');
insert into pm_app_shengquhua(id, provincecode, pname, jiancheng) values (f_newid, '610000', '陕西省', '陕');
insert into pm_app_shengquhua(id, provincecode, pname, jiancheng) values (f_newid, '620000', '甘肃省', '甘');
insert into pm_app_shengquhua(id, provincecode, pname, jiancheng) values (f_newid, '630000', '青海省', '青');
insert into pm_app_shengquhua(id, provincecode, pname, jiancheng) values (f_newid, '640000', '宁夏回族自治区', '宁');
insert into pm_app_shengquhua(id, provincecode, pname, jiancheng) values (f_newid, '650000', '新疆维吾尔自治区', '新');
insert into pm_app_shengquhua(id, provincecode, pname, jiancheng) values (f_newid, '710000', '台湾省', '台');
insert into pm_app_shengquhua(id, provincecode, pname, jiancheng) values (f_newid, '810000', '香港特别行政区', '港');
insert into pm_app_shengquhua(id, provincecode, pname, jiancheng) values (f_newid, '820000', '澳门特别行政区', '澳');


-- 插入市区划表pm_app_shiquhua
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '130100', '石家庄市', '130000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '130200', '唐山市', '130000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '130300', '秦皇岛市', '130000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '130400', '邯郸市', '130000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '130500', '邢台市', '130000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '130600', '保定市', '130000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '130700', '张家口市', '130000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '130800', '承德市', '130000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '130900', '沧州市', '130000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '131000', '廊坊市', '130000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '131100', '衡水市', '130000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '140100', '太原市', '140000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '140200', '大同市', '140000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '140300', '阳泉市', '140000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '140400', '长治市', '140000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '140500', '晋城市', '140000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '140600', '朔州市', '140000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '140700', '晋中市', '140000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '140800', '运城市', '140000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '140900', '忻州市', '140000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '141000', '临汾市', '140000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '141100', '吕梁市', '140000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '150100', '呼和浩特市', '150000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '150200', '包头市', '150000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '150300', '乌海市', '150000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '150400', '赤峰市', '150000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '150500', '通辽市', '150000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '150600', '鄂尔多斯市', '150000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '150700', '呼伦贝尔市', '150000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '150800', '巴彦淖尔市', '150000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '150900', '乌兰察布市', '150000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '152200', '兴安盟', '150000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '152500', '锡林郭勒盟', '150000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '152900', '阿拉善盟', '150000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '210100', '沈阳市', '210000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '210200', '大连市', '210000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '210300', '鞍山市', '210000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '210400', '抚顺市', '210000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '210500', '本溪市', '210000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '210600', '丹东市', '210000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '210700', '锦州市', '210000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '210800', '营口市', '210000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '210900', '阜新市', '210000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '211000', '辽阳市', '210000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '211100', '盘锦市', '210000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '211200', '铁岭市', '210000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '211300', '朝阳市', '210000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '211400', '葫芦岛市', '210000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '220100', '长春市', '220000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '220200', '吉林市', '220000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '220300', '四平市', '220000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '220400', '辽源市', '220000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '220500', '通化市', '220000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '220600', '白山市', '220000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '220700', '松原市', '220000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '220800', '白城市', '220000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '222400', '延边朝鲜族自治州', '220000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '230100', '哈尔滨市', '230000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '230200', '齐齐哈尔市', '230000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '230300', '鸡西市', '230000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '230400', '鹤岗市', '230000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '230500', '双鸭山市', '230000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '230600', '大庆市', '230000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '230700', '伊春市', '230000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '230800', '佳木斯市', '230000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '230900', '七台河市', '230000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '231000', '牡丹江市', '230000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '231100', '黑河市', '230000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '231200', '绥化市', '230000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '232700', '大兴安岭地区', '230000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '320100', '南京市', '320000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '320200', '无锡市', '320000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '320300', '徐州市', '320000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '320400', '常州市', '320000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '320500', '苏州市', '320000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '320600', '南通市', '320000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '320700', '连云港市', '320000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '320800', '淮安市', '320000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '320900', '盐城市', '320000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '321000', '扬州市', '320000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '321100', '镇江市', '320000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '321200', '泰州市', '320000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '321300', '宿迁市', '320000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '330100', '杭州市', '330000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '330200', '宁波市', '330000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '330300', '温州市', '330000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '330400', '嘉兴市', '330000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '330500', '湖州市', '330000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '330600', '绍兴市', '330000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '330700', '金华市', '330000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '330800', '衢州市', '330000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '330900', '舟山市', '330000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '331000', '台州市', '330000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '331100', '丽水市', '330000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '340100', '合肥市', '340000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '340200', '芜湖市', '340000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '340300', '蚌埠市', '340000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '340400', '淮南市', '340000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '340500', '马鞍山市', '340000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '340600', '淮北市', '340000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '340700', '铜陵市', '340000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '340800', '安庆市', '340000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '341000', '黄山市', '340000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '341100', '滁州市', '340000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '341200', '阜阳市', '340000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '341300', '宿州市', '340000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '341500', '六安市', '340000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '341600', '亳州市', '340000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '341700', '池州市', '340000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '341800', '宣城市', '340000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '350100', '福州市', '350000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '350200', '厦门市', '350000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '350300', '莆田市', '350000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '350400', '三明市', '350000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '350500', '泉州市', '350000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '350600', '漳州市', '350000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '350700', '南平市', '350000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '350800', '龙岩市', '350000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '350900', '宁德市', '350000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '360100', '南昌市', '360000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '360200', '景德镇市', '360000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '360300', '萍乡市', '360000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '360400', '九江市', '360000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '360500', '新余市', '360000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '360600', '鹰潭市', '360000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '360700', '赣州市', '360000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '360800', '吉安市', '360000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '360900', '宜春市', '360000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '361000', '抚州市', '360000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '361100', '上饶市', '360000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '370100', '济南市', '370000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '370200', '青岛市', '370000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '370300', '淄博市', '370000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '370400', '枣庄市', '370000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '370500', '东营市', '370000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '370600', '烟台市', '370000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '370700', '潍坊市', '370000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '370800', '济宁市', '370000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '370900', '泰安市', '370000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '371000', '威海市', '370000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '371100', '日照市', '370000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '371200', '莱芜市', '370000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '371300', '临沂市', '370000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '371400', '德州市', '370000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '371500', '聊城市', '370000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '371600', '滨州市', '370000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '371700', '菏泽市', '370000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '410100', '郑州市', '410000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '410200', '开封市', '410000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '410300', '洛阳市', '410000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '410400', '平顶山市', '410000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '410500', '安阳市', '410000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '410600', '鹤壁市', '410000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '410700', '新乡市', '410000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '410800', '焦作市', '410000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '410900', '濮阳市', '410000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '411000', '许昌市', '410000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '411100', '漯河市', '410000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '411200', '三门峡市', '410000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '411300', '南阳市', '410000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '411400', '商丘市', '410000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '411500', '信阳市', '410000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '411600', '周口市', '410000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '411700', '驻马店市', '410000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '419001', '济源市', '410000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '420100', '武汉市', '420000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '420200', '黄石市', '420000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '420300', '十堰市', '420000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '420500', '宜昌市', '420000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '420600', '襄阳市', '420000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '420700', '鄂州市', '420000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '420800', '荆门市', '420000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '420900', '孝感市', '420000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '421000', '荆州市', '420000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '421100', '黄冈市', '420000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '421200', '咸宁市', '420000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '421300', '随州市', '420000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '422800', '恩施土家族苗族自治州', '420000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '429004', '仙桃市', '420000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '429005', '潜江市', '420000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '429006', '天门市', '420000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '429021', '神农架林区', '420000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '430100', '长沙市', '430000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '430200', '株洲市', '430000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '430300', '湘潭市', '430000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '430400', '衡阳市', '430000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '430500', '邵阳市', '430000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '430600', '岳阳市', '430000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '430700', '常德市', '430000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '430800', '张家界市', '430000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '430900', '益阳市', '430000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '431000', '郴州市', '430000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '431100', '永州市', '430000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '431200', '怀化市', '430000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '431300', '娄底市', '430000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '433100', '湘西土家族苗族自治州', '430000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '440100', '广州市', '440000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '440200', '韶关市', '440000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '440300', '深圳市', '440000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '440400', '珠海市', '440000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '440500', '汕头市', '440000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '440600', '佛山市', '440000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '440700', '江门市', '440000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '440800', '湛江市', '440000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '440900', '茂名市', '440000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '441200', '肇庆市', '440000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '441300', '惠州市', '440000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '441400', '梅州市', '440000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '441500', '汕尾市', '440000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '441600', '河源市', '440000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '441700', '阳江市', '440000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '441800', '清远市', '440000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '441900', '东莞市', '440000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '442000', '中山市', '440000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '442101', '东沙群岛', '440000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '445100', '潮州市', '440000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '445200', '揭阳市', '440000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '445300', '云浮市', '440000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '450100', '南宁市', '450000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '450200', '柳州市', '450000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '450300', '桂林市', '450000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '450400', '梧州市', '450000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '450500', '北海市', '450000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '450600', '防城港市', '450000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '450700', '钦州市', '450000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '450800', '贵港市', '450000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '450900', '玉林市', '450000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '451000', '百色市', '450000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '451100', '贺州市', '450000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '451200', '河池市', '450000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '451300', '来宾市', '450000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '451400', '崇左市', '450000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '460100', '海口市', '460000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '460200', '三亚市', '460000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '460300', '三沙市', '460000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '460400', '儋州市', '460000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '469001', '五指山市', '460000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '469002', '琼海市', '460000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '469005', '文昌市', '460000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '469006', '万宁市', '460000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '469007', '东方市', '460000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '469021', '定安县', '460000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '469022', '屯昌县', '460000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '469023', '澄迈县', '460000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '469024', '临高县', '460000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '469025', '白沙黎族自治县', '460000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '469026', '昌江黎族自治县', '460000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '469027', '乐东黎族自治县', '460000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '469028', '陵水黎族自治县', '460000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '469029', '保亭黎族苗族自治县', '460000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '469030', '琼中黎族苗族自治县', '460000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '510100', '成都市', '510000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '510300', '自贡市', '510000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '510400', '攀枝花市', '510000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '510500', '泸州市', '510000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '510600', '德阳市', '510000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '510700', '绵阳市', '510000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '510800', '广元市', '510000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '510900', '遂宁市', '510000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '511000', '内江市', '510000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '511100', '乐山市', '510000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '511300', '南充市', '510000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '511400', '眉山市', '510000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '511500', '宜宾市', '510000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '511600', '广安市', '510000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '511700', '达州市', '510000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '511800', '雅安市', '510000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '511900', '巴中市', '510000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '512000', '资阳市', '510000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '513200', '阿坝藏族羌族自治州', '510000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '513300', '甘孜藏族自治州', '510000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '513400', '凉山彝族自治州', '510000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '520100', '贵阳市', '520000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '520200', '六盘水市', '520000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '520300', '遵义市', '520000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '520400', '安顺市', '520000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '520500', '毕节市', '520000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '520600', '铜仁市', '520000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '522300', '黔西南布依族苗族自治州', '520000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '522600', '黔东南苗族侗族自治州', '520000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '522700', '黔南布依族苗族自治州', '520000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '530100', '昆明市', '530000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '530300', '曲靖市', '530000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '530400', '玉溪市', '530000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '530500', '保山市', '530000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '530600', '昭通市', '530000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '530700', '丽江市', '530000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '530800', '普洱市', '530000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '530900', '临沧市', '530000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '532300', '楚雄彝族自治州', '530000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '532500', '红河哈尼族彝族自治州', '530000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '532600', '文山壮族苗族自治州', '530000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '532800', '西双版纳傣族自治州', '530000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '532900', '大理白族自治州', '530000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '533100', '德宏傣族景颇族自治州', '530000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '533300', '怒江傈僳族自治州', '530000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '533400', '迪庆藏族自治州', '530000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '540100', '拉萨市', '540000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '540200', '日喀则市', '540000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '540300', '昌都市', '540000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '540400', '林芝市', '540000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '540500', '山南市', '540000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '542400', '那曲地区', '540000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '542500', '阿里地区', '540000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '610100', '西安市', '610000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '610200', '铜川市', '610000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '610300', '宝鸡市', '610000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '610400', '咸阳市', '610000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '610500', '渭南市', '610000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '610600', '延安市', '610000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '610700', '汉中市', '610000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '610800', '榆林市', '610000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '610900', '安康市', '610000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '611000', '商洛市', '610000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '620100', '兰州市', '620000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '620200', '嘉峪关市', '620000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '620300', '金昌市', '620000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '620400', '白银市', '620000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '620500', '天水市', '620000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '620600', '武威市', '620000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '620700', '张掖市', '620000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '620800', '平凉市', '620000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '620900', '酒泉市', '620000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '621000', '庆阳市', '620000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '621100', '定西市', '620000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '621200', '陇南市', '620000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '622900', '临夏回族自治州', '620000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '623000', '甘南藏族自治州', '620000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '630100', '西宁市', '630000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '630200', '海东市', '630000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '632200', '海北藏族自治州', '630000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '632300', '黄南藏族自治州', '630000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '632500', '海南藏族自治州', '630000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '632600', '果洛藏族自治州', '630000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '632700', '玉树藏族自治州', '630000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '632800', '海西蒙古族藏族自治州', '630000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '640100', '银川市', '640000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '640200', '石嘴山市', '640000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '640300', '吴忠市', '640000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '640400', '固原市', '640000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '640500', '中卫市', '640000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '650100', '乌鲁木齐市', '650000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '650200', '克拉玛依市', '650000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '650400', '吐鲁番市', '650000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '650500', '哈密市', '650000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '652300', '昌吉回族自治州', '650000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '652700', '博尔塔拉蒙古自治州', '650000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '652800', '巴音郭楞蒙古自治州', '650000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '652900', '阿克苏地区', '650000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '653000', '克孜勒苏柯尔克孜自治州', '650000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '653100', '喀什地区', '650000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '653200', '和田地区', '650000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '654000', '伊犁哈萨克自治州', '650000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '654200', '塔城地区', '650000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '654300', '阿勒泰地区', '650000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '659001', '石河子市', '650000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '659002', '阿拉尔市', '650000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '659003', '图木舒克市', '650000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '659004', '五家渠市', '650000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '659005', '北屯市', '650000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '659006', '铁门关市', '650000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '659007', '双河市', '650000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '659008', '可克达拉市', '650000');
insert into pm_app_shiquhua(id, citycode, cname, provincecode) values (f_newid, '659009', '昆玉市', '650000');

~~~
