**Note:** This version is reserved for parsing user: names, tags and IDs.\
**Instructions**\
* Replace `DO_THIS` with the code you want to run if validation is successful.\
* Replace `ELSE_DO_THIS` with the code you want to run if validation is invalid.\

**Code**
```sh
{if;{utils.isSnowflake;{user.id;{args}}};
  DO_THIS
  ;
  ELSE_DO_THIS
}
```
