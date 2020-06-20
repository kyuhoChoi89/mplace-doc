---
title: Define mplace db schema  
---
# Define mplace db schema

| Product | mplace               |
| ------- | -------------------- |
| Author  | jonglyul Park        |
| Date    | 2020-06-18           |


## Overview

This feature define mplace service databse schema.

## Goals and Non-Goal

## Libraries

The following libraries and their dependencies will be used:

| Library | Version |Reason |
|:---|:---|:---|
| mysql2 | `^2.0.2`(Undetermined) | Connect to Aurora of AWS RDS |

## Database definition

### Table: USER

- 유저정보를 담은 테이블

#### Columns:

| Column Name | Data Type   | NULL | Default   | KEY | Extra 
| ---         | ---         | ---  | ---       | --- | ---
| id          | INT         | NO   | -         | PK  | auto_increment for user id
| userId      | VARCHAR(50) | NO   | -         | PK  | user Id
| password    | VARCHAR(50) | NO   | -     |     | password for user
| name        | VARCHAR(50) | NO   | -     |     |
| age         | INT         | NO   | -     |     |
| placebook   | VARCHAR(50) | NO   | -         |     | 가이드북리스트 연동??
| USER_NUMBER | INT         | NO   | -         |     | 테이블 데이터개수??
| regist_date | DATETIME    | NO   | CURDATE   |     |
| regist_user | INT         | NO   | -         |     |
| update_date | DATETIME    | NO   | CURDATE   |     |
| update_user | INT         | NO   | -         |     |

### Table: FRIEND_LIST

- 친구테이블 유저A -(친구수락=열람허가)-> 유저B : 유저B는 A의 가이드북 열람가능

#### Columns:

| Column Name | Data Type   | NULL | Default   | KEY | Extra 
| ---         | ---         | ---  | ---       | --- | ---
| USER_ID_A   | VARCHAR(50)         | NO   | -         |   | 사용자A  친구요청수락
| USER_ID_B   | VARCHAR(50) | NO   | -         |   | 사용자B  친구요청자
| FRIEND_SETTING    | VARCHAR(50) | NO   | -     | FK  | 기본:공개 , 숨김이나 차단시 변경
| FRIEND_LIST_NUMBER        | VARCHAR(50) | NO   | -     |     | 테이블 데이터개수 
| regist_date | DATETIME    | NO   | CURDATE   |     |
| regist_user | INT         | NO   | -         |     |
| update_date | DATETIME    | NO   | CURDATE   |     |
| update_user | INT         | NO   | -         |     |

### Table: FRIEND_SETTING

- 유저정보를 담은 테이블

#### Columns:

| Column Name | Data Type   | NULL | Default   | KEY | Extra 
| ---         | ---         | ---  | ---       | --- | ---
| FRIEND_SETTING          | VARCHAR(50)   | NO   | -         |  PK | 상태표시
| hide      | VARCHAR(50) | NO   | -         |   | 숨김여부
| block    | VARCHAR(50) | NO   | -     |     | 차단여부
| regist_date | DATETIME    | NO   | CURDATE   |     |
| regist_user | INT         | NO   | -         |     |
| update_date | DATETIME    | NO   | CURDATE   |     |
| update_user | INT         | NO   | -         |     |


### Table: PlACEBOOK_LIST

- 

#### Columns:

| Column Name | Data Type   | NULL | Default   | KEY | Extra 
| ---         | ---         | ---  | ---       | --- | ---
| placebook          | VARCHAR(50)         | NO   | -         | PK  | 
| PLACE_NUMBER      | VARCHAR(50) | NO   | -         |   | 
| PlACE_NAME    | VARCHAR(50) | NO   | -     |     | 
| location        | VARCHAR(50) | NO   | -     |     |
| date         | DATETIME         | NO   | -     |     |
| post   | VARCHAR(50) | NO   | -         |  FK  | 
| regist_date | DATETIME    | NO   | CURDATE   |     |
| regist_user | INT         | NO   | -         |     |
| update_date | DATETIME    | NO   | CURDATE   |     |
| update_user | INT         | NO   | -         |     |


### Table: POST_LIST

- 

#### Columns:

| Column Name | Data Type   | NULL | Default   | KEY | Extra 
| ---         | ---         | ---  | ---       | --- | ---
| POST          | INT         | NO   | -         | PK  | 
| POST_NUMBER      | VARCHAR(50) | NO   | -         |   | 
| POST_NAME    | VARCHAR(50) | NO   | -     |     | 
| location        | VARCHAR(50) | NO   | -     |     |
| date         | INT         | NO   | -     |     |
| picture   | VARCHAR(50) | NO   | -         |     | 
| regist_date | DATETIME    | NO   | CURDATE   |     |
| regist_user | INT         | NO   | -         |     |
| update_date | DATETIME    | NO   | CURDATE   |     |
| update_user | INT         | NO   | -         |     |








