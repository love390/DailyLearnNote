## liquibase

AbstractSqlStatement：修改表结构的抽象类，存在很多相关子类。

 Database database = DatabaseFactory.getInstance().findCorrectDatabaseImplementation(jdbcConnection);
 AddColumnStatement statement = new AddColumnStatement();
 ExecutorService.getInstance().getExecutor(database).execute(statement);
