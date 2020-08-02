use mplace;
CREATE TABLE USER(
 user_id      INT          NOT NULL   PRIMARY KEY ,
 login_id     VARCHAR(50)  NOT NULL  ,
 password     VARCHAR(50)  NOT NULL  ,
 name         VARCHAR(50)  NOT NULL  ,
 age          INT                    ,            
 email        VARCHAR(50)            ,           
 regist_date  DATETIME     NOT NULL  ,
 regist_user  INT          NOT NULL  ,
 update_date  DATETIME     NOT NULL  ,
 update_user  INT          NOT NULL  
 );

CREATE TABLE FREIND(
 friend_id     INT         NOT NULL    PRIMARY KEY  ,
 receiver_id   INT         NOT NULL       ,
 requester_id  INT         NOT NULL       ,
 deleted       INT         NOT NULL       ,
 accepted      INT              ,
 blocked       INT              ,
 regist_date   DATETIME    NOT NULL   ,
 regist_user   INT         NOT NULL   ,
 update_date   DATETIME    NOT NULL   ,
 update_user   INT         NOT NULL   

);

CREATE TABLE PLACEBOOK(
placebook_id  INT          NOT NULL   PRIMARY KEY  ,
user_id       INT          NOT NULL    ,
title         VARCHAR(50)  NOT NULL    ,
image_name    VARCHAR(50)  NOT NULL    ,
regist_date   DATETIME     NOT NULL    ,
regist_user   INT          NOT NULL    ,
update_date   DATETIME     NOT NULL    ,
update_user   INT          NOT NULL    
);

CREATE TABLE POST(
	post_id	CHAR(30)  		PRIMARY KEY,
    user_id	INT  			NOT NULL,
    placebook_id INT  		NOT NULL,
    title	VARCHAR(50) 	NOT NULL,
    content	VARCHAR(2048) 	NOT NULL,
    rate	DOUBLE  		NOT NULL,
    location	VARCHAR(50) NOT NULL,
    regist_date DATETIME 	NOT NULL ,
	regist_user INT  		NOT NULL,
	update_date  DATETIME 	NOT NULL ,
	update_user  INT       	NOT NULl

);

CREATE TABLE POST_IMAGE(
	image_id     INT          	NOT NULL   PRIMARY KEY ,
	post_id      INT          	NOT NULL      ,
	image_name   VARCHAR(2048)  NOT NULL        ,
	regist_date  DATETIME     	NOT NULL      ,
	regist_user  INT          	NOT NULL      ,
	update_date  DATETIME     	NOT NULL      ,
	update_user  INT          	NOT NULL      
);


