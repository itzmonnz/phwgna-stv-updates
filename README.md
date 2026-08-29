# phwgna STV updates

Kho công khai tối thiểu chỉ dùng để phát hành metadata cập nhật đã ký cho
**phwgna STV AI Translator**. Kho này không chứa mã nguồn tiện ích, dữ liệu DOM,
prompt, nội dung truyện hoặc dữ liệu người dùng.

Tiện ích chỉ đọc `latest.json` và chỉ hiển thị bản cập nhật khi:

- chữ ký Ed25519 khớp khóa chủ sở hữu đã ghim trong tiện ích;
- phiên bản mới hơn phiên bản đang cài;
- `releaseUrl` trỏ đúng GitHub Releases của kho này;
- metadata đúng schema giới hạn bên dưới.

`latest.json` được tạo từ repo private bằng lệnh `npm run release:update-metadata`.
Không chỉnh tay hoặc đăng metadata chưa ký.

## Schema

```json
{
  "version": "1.2.3",
  "releaseUrl": "https://github.com/itzmonnz/phwgna-stv-updates/releases/tag/v1.2.3",
  "sha256": "64 lowercase hex characters",
  "publishedAt": "2026-08-29T00:00:00.000Z",
  "signature": "Ed25519 signature in base64"
}
```

Không có cơ chế tự cài hoặc tải mã thực thi từ xa. Người dùng chủ động bấm
**Mở bản mới** để xem GitHub Release.
