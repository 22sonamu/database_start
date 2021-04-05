![image](https://user-images.githubusercontent.com/73538957/113555064-46314800-9635-11eb-8d4e-53f1c9298e8b.png)


## 테이블로 나타내기

![image](https://user-images.githubusercontent.com/73538957/113555211-7c6ec780-9635-11eb-877c-fc8dd3a8b607.png)


## sql 언어로 나타내기 (Player)

```mysql
CREATE TABLE [PLAYER]
(
 [Player_id] integer NOT NULL ,
 [Name]      varchar(45) NOT NULL ,
 [Position]  char(2) NULL ,
 [Back_no]   int NULL ,
 [Team_id]   integer NULL ,


 CONSTRAINT [PK_player] PRIMARY KEY CLUSTERED ([Player_id] ASC),
 CONSTRAINT [FK_25] FOREIGN KEY ([Team_id])  REFERENCES [TEAM]([Team_id])
);
GO


CREATE NONCLUSTERED INDEX [fkIdx_26] ON [PLAYER] 
 (
  [Team_id] ASC
 )

GO
```

