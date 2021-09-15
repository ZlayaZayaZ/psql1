## PSQL-запросы
#
### create table Musician (
#### id serial primary key,
#### name varchar(50) not null unique
### );
#
### create table Genre (
#### id serial primary key,
#### name_genre varchar(50) not null unique,
#### musician_id integer references Musician(id)
### );
#
### create table Album (
#### id serial primary key,
#### name_album varchar(50) not null,
#### released integer not null,
#### musician_id integer references Musician(id)
### );
#
### create table Track (
#### id serial primary key,
#### name_track varchar(50) not null,
#### duration integer not null,
#### album_id integer references Album(id)
### );

