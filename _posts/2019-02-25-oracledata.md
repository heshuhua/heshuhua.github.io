---
layout: post
title:  oracledata
date:   2019-02-25 09:00:00 +0800
categories: engineering
---
oracle 数据的导入导出
### oracle 导入导出

--从测试环境备份数据命令
expdp DH_PRODUCT/dh@orcl schemas=DFYH_DMS dumpfile =DH_PRODUCT1224.dmp logfile=DH_PRODUCT1224.log job_name=DH_PRODUCT1

sqlplus/nolog
--创建表空间
create tablespace DFYH_DMS logging datafile 'D:\app\Administrator\oradata\orcl\DFYH_DMS.dbf' size 2000M autoextend on next 1000M maxsize unlimited extent management local segment space management auto;


C:\app\heshuhua\oradata\orcl

create tablespace PRODUCT65 logging datafile 'c:\app\heshuhua\oradata\orcl\PRODUCT.dbf' size 2000M autoextend on next 1000M maxsize unlimited extent management local segment space management auto;
--创建临时表空间
create temporary tablespace DFYH_DMS_TEMP tempfile 'D:\app\Administrator\oradata\orcl\DFYH_DMS_TEMP.dbf' size 50m autoextend on next 50m maxsize 20480m extent management local;

create temporary tablespace PRODUCT_TEMP tempfile 'c:\app\heshuhua\oradata\orcl\PRODUCT_TEMP.dbf' size 50m autoextend on next 50m maxsize 20480m extent management local;

-- 创建用户
create user dfyh_dms identified by dh default tablespace DFYH_DMS temporary tablespace DFYH_DMS_TEMP;

create user product65 identified by dh default tablespace PRODUCT65 temporary tablespace PRODUCT_TEMP;

-- 创建用户的文件路径，可不要
grant execute, read, write on directory SYS.DIR_DP to dfyh_dms with grant option;

grant execute, read, write on directory SYS.DIR_DP to product65 with grant option;


-- Grant/Revoke role privileges
grant connect to dfyh_dms;

grant connect to product65;


grant dba to dfyh_dms;

grant dba to product65;

grant resource to dfyh_dms;

grant resource to product65;

-- Grant/Revoke system privileges
grant unlimited tablespace to dfyh_dms;

grant unlimited tablespace to product65;


--修改用户密码
alter user dfyh_dms identified by dfyhdms2016pwd;

alter user product65 identified by dh;


--登录
sqlplus / as sysdba
sqlplus /nolog
connect dfyh_dms/dfyhdms2016pwd@orcl

connect product65/dh@orcl

--删除用户，创建错误时使用
drop user dfyh_dms cascade;

drop user product65 cascade;

--删除表空间，创建错误时使用
drop tablespace DFYH_DMS including contents and datafiles;


impdp dfyh_dms/dfyhdms2016pwd  DUMPFILE=DH_PRODUCT1224.DMP REMAP_SCHEMA=DH_PRODUCT:DFYH_DMS remap_tablespace=(DINGHONG_PRODUCT:DFYH_DMS)

impdp product65/dh  DUMPFILE=PRODUCT1220.DMP REMAP_SCHEMA=PRODUCT65:product65 remap_tablespace=(product65:product65)

impdp eb_bear/ec DUMPFILE=eb_bear130730.dmp REMAP_SCHEMA=eb_bear:eb_bear remap_tablespace=(EBRIDGE_XIAOXIONG:EBRIDGE_BEAR,EBRIDGE_LB:EBRIDGE_BEAR,EASYBRIDGE:EBRIDGE_BEAR)
