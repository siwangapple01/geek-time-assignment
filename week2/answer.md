本周问题：我们在数据库操作的时候，比如 dao 层中当遇到一个 sql.ErrNoRows 的时候，是否应该 Wrap 这个 error，抛给上层。为什么，应该怎么做请写出代码？

-   如果在 DAO 层碰到 `sql.ErrNoRows`的错误的时候，我们应该用 Wrap 把 error 抛给上层处理
-   代码示例：
    ```
     return errors.Wrapf(code.NotFound, fmt.Sprintf("sql: %s error: %v", sql, err))
    ```

```

```
