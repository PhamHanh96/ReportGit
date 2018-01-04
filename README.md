# ReportGit
This is my ReportGit

2. Các lệnh cơ bản của git
 + Để khởi tạo Git trong một repository (repo), bạn chỉ cần gõ câu lệnh sau. Nếu bạn không khởi tạo Git, bạn không thể sử dụng bất kì các câu lệnh Git nào cả.
    Cú pháp : git init


 + Sao chép (clone) một repository
   - Để clone 1 repository có sẵn ở trên máy cục bộ, bạn hãy sử dụng dòng lệnh sau:
      Cú pháp : git clone /đường-dẫn-đến/repository/

   - Nếu repository đó ở máy chủ khác thì bạn hãy gõ dòng lệnh sau:
      Cú pháp : git clone tênusername@địachỉmáychủ:/đường-dẫn-đến/repository


   - Trên máy local, kho mã nguồn của bạn sẽ chứa 3 cây “trees” được quản lý bởi git.1)thứ nhất chính là thư mục làm việc của bạn Working Directory, mà chứa các file bạn làm việc. 2) thứ 2 là bộ chỉ mục Index mà nó chứa các giai đoạn phát triển các phiên bản và 3) cuối cùng là Head trỏ đến phiên bản mà bạn đánh dấu lần cuối cùng.
       https://imgur.com/a/LoSVw
     Để đánh dấu thay đổi và đưa mã nguồn vào bộ Index, sử dụng:
     Cú pháp: git add <tên-tập-tin>
     hoặc
     Cú pháp : git add *

   - Để thật sự commit những thay đổi, bạn sử dụng:
     Cú pháp: git commit -m "Ghi chú Commit"