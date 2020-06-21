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
| user_id      | INT         | NO   | -        | PK  | auto_increment for user id
| login_id    | VARCHAR(50) | NO   | -         |     | user Id ex. kyuho.choi
| password    | VARCHAR(50) | NO   | -     |     | password for user ex. password
| name        | VARCHAR(50) | NO   | -     |     | nickname ex. nickname
| age         | INT         |      | -     |     |
| email       | VARCHAR(50) |      | -     |     |
| regist_date | DATETIME    | NO   | CURDATE   |     |
| regist_user | INT         | NO   | -         |     |
| update_date | DATETIME    | NO   | CURDATE   |     |
| update_user | INT         | NO   | -         |     |

### Table: FRIEND

- 

#### Columns:

| Column Name  | Data Type   | NULL | Default   | KEY | Extra 
| ---          | ---         | ---  | ---       | --- | ---
| friend_id    | INT         | NO   | -         | PK  | auto_increment for friend table
| receiver_id  | INT         | NO   | -         |     | 사용자A  친구요청수락 ex. 1(kyuho)
| requester_id | INT         | NO   | -         |     | 사용자B  친구요청자 ex. 2(jonglyul)
| deleted      | INT         | NO   | -         |     | 0 아직 처리되지 않은 요청 1 이미 처리된 요청
| accepted     | INT         |      | -         |     | 0 친구 승낙이 받아들여지지 않음 1 친구 요청 승낙됨
| blocked      | INT         |      | -         |     | 0 아직 친구 1 절교
| regist_date  | DATETIME    | NO   | CURDATE   |     |
| regist_user  | INT         | NO   | -         |     |
| update_date  | DATETIME    | NO   | CURDATE   |     |
| update_user  | INT         | NO   | -         |     |


### Table: PlACEBOOK

- 마이 플레이스 모음집

#### Columns:

| Column Name | Data Type   | NULL | Default   | KEY | Extra 
| ---         | ---         | ---  | ---       | --- | ---
| placebook_id| INT         | NO   | -         | PK  | auto_increment for PlACEBOOK table
| user_id      | INT         | NO   | -     |     | placebook owner id
| title       | VARCHAR(50) | NO   | -     |     | title 
| image_name  | VARCHAR(50) | NO   | -     |     | directory for image
| regist_date | DATETIME    | NO   | CURDATE   |     |
| regist_user | INT         | NO   | -         |     |
| update_date | DATETIME    | NO   | CURDATE   |     |
| update_user | INT         | NO   | -         |     |


### Table: POST

- 

#### Columns:

| Column Name | Data Type   | NULL | Default   | KEY | Extra 
| ---         | ---         | ---  | ---       | --- | ---
| post_id     | INT         | NO   | -         | PK  | auto_increment for POST table
| user_id     | INT         | NO   | -     |     | placebook owner id
| placebook_id| INT         | NO   | -         | FK  | PlACEBOOK table id
| title       | VARCHAR(50) | NO   | -         |     | title
| content     | VARCHAR(2048) | NO   | -     |     | contents 
| rate        | DOUBLE      | NO   | -     |     | rate
| location    | VARCHAR(50) | NO   | -     |     | 위도 경도 값 38, 40
| regist_date | DATETIME    | NO   | CURDATE   |     |
| regist_user | INT         | NO   | -         |     |
| update_date | DATETIME    | NO   | CURDATE   |     |
| update_user | INT         | NO   | -         |     |


### Table: POST_IMAGE

- 

#### Columns:

| Column Name | Data Type   | NULL | Default   | KEY | Extra 
| ---         | ---         | ---  | ---       | --- | ---
| image_id    | INT         | NO   | -         | PK  | auto_increment for POST_IMAGE table
| post_id     | INT         | NO   | -         |     | placebook owner id
| image_name  | VARCHAR(2048) | NO   | -       |     | directory for image 
| regist_date | DATETIME    | NO   | CURDATE   |     |
| regist_user | INT         | NO   | -         |     |
| update_date | DATETIME    | NO   | CURDATE   |     |
| update_user | INT         | NO   | -         |     |





