# Docker Volume - Session 09

## 1. Tạo Named Volume

```bash
docker volume create easy-volume
```

## 2. Ghi dữ liệu vào Volume

```bash
docker run --rm -v easy-volume:/data alpine sh -c "echo 'Luu tru du lieu Docker' > /data/test.txt"
```

## 3. Đọc dữ liệu từ Volume

```bash
docker run --rm -v easy-volume:/data alpine cat /data/test.txt
```

**Kết quả:**

```text
Luu tru du lieu Docker
```

## 4. Kiểm tra danh sách Volume

```bash
docker volume ls
```

**Kết quả:** Có Volume `easy-volume`.

## 5. Kiểm tra dữ liệu sau khi container đã bị xóa

```bash
docker run --rm -v easy-volume:/data alpine cat /data/test.txt
```

**Kết quả:**

```text
Luu tru du lieu Docker
```
