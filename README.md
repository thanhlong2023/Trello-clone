cách xóa commit trong branch
https://graphite.dev/guides/how-to-delete-a-git-commit

1.Cấu hình hành vi kết thúc dòng của Git:

Mở terminal hoặc cửa sổ lệnh trong thư mục dự án của bạn.

Chạy lệnh sau để kiểm tra cấu hình Git hiện tại cho ký tự kết thúc dòng:

Bash
git config --global core.autocrlf

Kết quả sẽ là true (chuyển đổi tự động), false (không chuyển đổi) hoặc input (chuyển đổi khi commit, giữ nguyên khi checkout).

Chọn cài đặt phù hợp dựa trên sở thích của bạn:

Để sử dụng LF thống nhất trên tất cả các hệ thống (bao gồm Windows), hãy đặt core.autocrlf thành input:

Bash
git config --global core.autocrlf input

Để tự động chuyển đổi sang CRLF trên Windows và giữ nguyên LF trên các hệ thống khác, hãy đặt core.autocrlf thành true:

Bash
git config --global core.autocrlf true

2. Chuẩn hóa thủ công ký tự kết thúc dòng (chỉ thực hiện một lần):

Nếu bạn muốn xử lý ký tự kết thúc dòng thủ công một lần, hãy sử dụng cờ --renormalize với git add:

Bash
git add --renormalize README.md

Lệnh này sẽ chuyển đổi ký tự kết thúc dòng trong README.md để phù hợp với mặc định của hệ thống bạn và cập nhật chỉ mục Git cho phù hợp.

Chọn cách phù hợp:

Nếu bạn cộng tác với các nhà phát triển trên các hệ điều hành khác nhau, hãy đặt core.autocrlf thành input để đảm bảo sử dụng LF thống nhất.
Nếu bạn chủ yếu làm việc trên Windows và muốn chuyển đổi tự động sang CRLF, hãy đặt core.autocrlf thành true.
