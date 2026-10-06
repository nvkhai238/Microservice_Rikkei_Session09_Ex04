# Session 09 - Bài 04

Config Server chạy ở `8888`, Pharmacy-Service ở `8090`. Cấu hình dùng trong bài nằm tại `pharmacy-config-repo/pharmacy-service.properties` và được Config Server đọc từ Git của repo này. PostgreSQL chạy ở cổng `5433`.

## Chạy

```bash
git status --short
git add pharmacy-config-repo/pharmacy-service.properties
git commit -m 'Update pharmacy config'
cd config-server && gradle bootRun
```

Terminal khác:

```bash
docker compose up -d
cd pharmacy-service && gradle bootRun
```

## Bài 04

Thêm fallback tồn kho cục bộ khi kho tổng lỗi, kèm thông báo hướng dẫn tiếp tục giao dịch.
