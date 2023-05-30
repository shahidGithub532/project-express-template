# create database

```
>npx sequelize db:create
```

### Database tables managed by model

`create database model. In other words create table using sequelize CLI`

```
>npx sequelize model:generate --name Airplane --attributes modelNumber:string,capacity:integer
```

<p>after this command the sequelize created two files "airplane.js" and "------create-airplane.js"
It doesn't create table in your database.
</p>

### now migrate the model

<p>This Migration will create the database table 
there are two functions available in model up() and down()
up() for create table
down() destroy table</p>

```
> npx sequelize db:migrate
```

### revert from migration

```
> npx sequelize db:migrate:undo
```

### revert all migration
```
> npx sequelize db:migrate:all

```
Note: while db:migrate:undo the down() function will apply
    and while db:migrate the up() function will apply
```

`constrains`
There two type of constraints we can give one at database level
and another at javascript level(any language being used in backend)
