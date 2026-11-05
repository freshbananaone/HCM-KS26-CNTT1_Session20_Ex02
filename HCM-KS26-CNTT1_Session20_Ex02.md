# Bài 2: Chuỗi tấn công từ mật khẩu bị rò rỉ

## 1. Cơ chế tấn công dây chuyền

Khi một diễn đàn công nghệ nhỏ bị lộ dữ liệu, hacker có thể lấy được danh sách email và mật khẩu của người dùng. Nếu tôi dùng cùng mật khẩu `123456` cho diễn đàn, Gmail, Facebook và GitHub thì chỉ cần một tài khoản bị lộ, các tài khoản còn lại cũng có nguy cơ bị chiếm đoạt.

Hacker thường dùng kỹ thuật **Credential Stuffing**: lấy email và mật khẩu đã rò rỉ để thử đăng nhập tự động trên nhiều trang web khác nhau. Nếu đăng nhập được vào Gmail, họ còn có thể lợi dụng chức năng **Quên mật khẩu** để tìm cách kiểm soát thêm những tài khoản liên kết với email đó.

Đó là **hiệu ứng domino**: một tài khoản nhỏ bị tấn công có thể kéo theo hàng loạt tài khoản quan trọng khác.

## 2. Vì sao mật khẩu tự nghĩ ra dễ bị bẻ khóa?

Mật khẩu như `123456`, ngày sinh, tên riêng hoặc các dãy số quen thuộc rất dễ đoán. Nhiều người có thói quen chọn mật khẩu ngắn, dễ nhớ nên hacker có thể thử chúng bằng danh sách mật khẩu phổ biến hoặc công cụ tự động.

Ngược lại, mật khẩu được máy tính tạo ngẫu nhiên, chẳng hạn `vK8!q2#L9p@T4z`, khó đoán hơn vì không theo quy luật quen thuộc. Khi mật khẩu đủ dài và được tạo ngẫu nhiên bằng công cụ đáng tin cậy, số khả năng phải thử sẽ lớn hơn rất nhiều.

Vì vậy, mỗi tài khoản nên có **một mật khẩu mạnh và riêng biệt**, thay vì dùng chung một mật khẩu cho tất cả.

## 3. Vì sao nên dùng Password Manager có AES-256?

**AES-256** là thuật toán mã hóa dữ liệu sử dụng khóa dài 256 bit. Nhiều ứng dụng quản lý mật khẩu  dùng AES-256 để **mã hóa kho mật khẩu** trước khi lưu trữ. Muốn đọc được dữ liệu đã mã hóa, người khác phải có khóa giải mã phù hợp.

Password Manager giúp tôi:

- Lưu mật khẩu dưới dạng được mã hóa thay vì ghi chúng vào một tệp văn bản thông thường.
- Tạo mật khẩu dài, ngẫu nhiên và khác nhau cho từng tài khoản.
- Không cần nhớ hàng chục mật khẩu, chỉ cần bảo vệ tốt **Master Password**.

Ví dụ, nếu tôi ghi mọi mật khẩu vào một tệp ghi chú không mã hóa rồi làm lộ tệp đó, người khác có thể đọc được ngay. Còn với Password Manager được thiết kế tốt, dữ liệu trong kho đã được mã hóa nên khó bị đọc trực tiếp hơn khi tệp lưu trữ bị đánh cắp.

Tuy nhiên, **AES-256 không có nghĩa là an toàn tuyệt đối**. Nếu Master Password quá yếu, thiết bị nhiễm mã độc hoặc tôi nhập mật khẩu vào trang giả mạo thì tài khoản vẫn có thể bị xâm nhập. Ghi mật khẩu trên giấy và cất kín cũng có thể tránh được một số rủi ro trực tuyến, nhưng bất tiện khi sử dụng nhiều tài khoản.

## 4. Cách phòng tránh

Tôi sẽ đổi ngay những mật khẩu đã dùng chung, bắt đầu từ Gmail, sau đó đến Facebook, GitHub và diễn đàn. Tiếp theo, tôi bật **xác thực hai yếu tố (2FA)**, kiểm tra các phiên đăng nhập lạ và sử dụng Password Manager để tạo mật khẩu riêng cho từng tài khoản.


