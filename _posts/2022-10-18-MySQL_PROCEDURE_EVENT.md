---
layout: post
title: MySQL 프로시저, 이벤트 생성
category: MySQL
tags: [mysql, event, procedure]
---

### CREATE PROCEDURE

```sql
CREATE PROCEDURE test_proc()
BEGIN
  SELECT now();
END $$
DELIMITER ;
```

### CREATE EVENT

```sql
CREATE EVENT test_proc
ON SCHEDULE EVERY 15 DAY_HOUR
COMMENT '매일 15시 실행'
DO CALL unpaid_proc();
```
