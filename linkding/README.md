## 创建超级用户

修改 `joe` 和 `joe@example.com` 为超级用户的用户名和密码

```bash
sudo docker-compose exec linkding python manage.py createsuperuser --username=joe --email=joe@example.com
```

然后输入两次这个用户的密码

## Ref

- [VPS · 搭建轻量便捷的书签应用 Linkding | Seviche.cc](https://seviche.cc/2022-12-18-linkding-intro/)
- [linkding/docker-compose.yml at master · sissbruecker/linkding · GitHub](https://github.com/sissbruecker/linkding/blob/master/docker-compose.yml)
