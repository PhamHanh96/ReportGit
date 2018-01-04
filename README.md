# ReportGit
This is my ReportGit
<<<<<<< HEAD

2. Các lệnh cơ bản của git
 + Để khởi tạo Git trong một repository (repo), bạn chỉ cần gõ câu lệnh sau. Nếu bạn không khởi tạo Git, bạn không thể sử dụng bất kì các câu lệnh Git nào cả.
    Cú pháp : git init


 + Sao chép (clone) một repository
   - Để clone 1 repository có sẵn ở trên máy cục bộ, bạn hãy sử dụng dòng lệnh sau:
      Cú pháp : git clone /đường-dẫn-đến/repository/

   - Nếu repository đó ở máy chủ khác thì bạn hãy gõ dòng lệnh sau:
      Cú pháp : git clone tênusername@địachỉmáychủ:/đường-dẫn-đến/repository


  + Trên máy local, kho mã nguồn của bạn sẽ chứa 3 cây “trees” được quản lý bởi git.1)thứ nhất chính là thư mục làm việc của bạn Working Directory, mà chứa các file bạn làm việc. 2) thứ 2 là bộ chỉ mục Index mà nó chứa các giai đoạn phát triển các phiên bản và 3) cuối cùng là Head trỏ đến phiên bản mà bạn đánh dấu lần cuối cùng.
       https://imgur.com/a/LoSVw
     Để đánh dấu thay đổi và đưa mã nguồn vào bộ Index, sử dụng:
       Cú pháp: git add <tên-tập-tin>
     hoặc
       Cú pháp : git add *

   - Để thật sự commit những thay đổi, bạn sử dụng:
<<<<<<< HEAD
     Cú pháp: git commit -m "Ghi chú Commit"
=======
1. Sơ đồ tổng quan về hệ thống Git.
- Git là tên gọi của một Hệ thống quản lý phiên bản phân tán (Distributed Version Control System – DVCS) là một trong những hệ thống quản lý phiên bản phân tán phổ biến nhất hiện nay.
- DVCS nghĩa là hệ thống giúp mỗi máy tính có thể lưu trữ nhiều phiên bản khác nhau của một mã nguồn được nhân bản (clone) từ một kho chứa mã nguồn (repository), mỗi thay đổi vào mã nguồn trên máy tính sẽ có thể ủy thác (commit) rồi đưa lên máy chủ nơi đặt kho chứa chính. Và một máy tính khác (nếu họ có quyền truy cập) cũng có thể clone lại mã nguồn từ kho chứa hoặc clone lại một tập hợp các thay đổi mới nhất trên máy tính kia. Trong Git, thư mục làm việc trên máy tính gọi là Working Tree.
 https://imgur.com/a/Q4sDa
- Tại sao nên sử dụng Git?
  Có rất nhiều lợi thế để bạn nên sử dụng Git trong việc lập trình ngay từ hôm nay, bất kể là lập trình cái gì đi chăng nữa.
  + Git dễ sử dụng, an toàn và nhanh chóng.
  + Có thể giúp quy trình làm việc code theo nhóm đơn giản hơn rất nhiều bằng việc kết hợp các phân nhánh (branch).
  + Bạn có thể làm việc ở bất cứ đâu vì chỉ cần clone mã nguồn từ kho chứa hoặc clone một phiên bản thay đổi nào đó từ kho chứa, hoặc một nhánh nào đó từ kho chứa.
  + Dễ dàng trong việc deployment sản phẩm.
3. Cách sử dụng .gitignore
- Gitignore là gì?
  Gitignore là file có tên là .gitignore do thằng Git quy định, nhiệm vụ của nó là liệt kê những file mà mình không mong muốn cho vào git hoặc hiểm nôm na là thằng Git sẽ lờ những file đó đi.
- Cách thức hoạt động: Khi add 1 file mới vào git, git sẽ kiểm tra danh sách những thằng sẽ lờ đi trong file .gitignore và lờ luôn chúng nó. Đó mới chỉ là điều kiện cần, điều kiện đủ là nó không có trong git cache nữa thì thằng git nó mới lờ đi chứ nó mà nằm trong git cache thì .gitignore sẽ vô tác dụng.
- Git thấy mọi tệp trong bản sao làm việc của bạn là một trong ba điều sau:
  + Theo dõi - một tập tin đã được dàn dựng hoặc cam kết.
  + Untracked - một tập tin đã không được hiển thị hoặc cam kết. 
  + Bị bỏ qua - một tệp tin mà Git đã được nói rõ ràng để bỏ qua.
- Các tệp bị bỏ qua thường tạo các hiện vật và các tệp được máy tạo ra có thể được lấy từ nguồn lưu trữ của bạn hoặc nếu không được cam kết. Một số ví dụ phổ biến là:
  + Cache phụ thuộc, chẳng hạn như nội dung của /node_moduleshay/packages
  + Biên dịch mã, chẳng hạn như .o, .pycvà .classfile
  + Xây dựng thư mục đầu ra, chẳng hạn như /bin, /outhoặc/target
  + Tập tin được tạo trong thời gian chạy, chẳng hạn như .log, .lockhoặc.tmp
  + Tập tin hệ thống ẩn, chẳng hạn như .DS_StorehayThumbs.db
  + Tệp cấu hình IDE cá nhân, chẳng hạn như .idea/workspace.xml
- Các tệp bị bỏ qua được theo dõi trong một tệp đặc biệt có tên .gitignoređược kiểm tra tại thư mục gốc của kho lưu trữ của bạn. Không có lệnh git ignore rõ ràng: thay vào đó .gitignoretệp tin phải được chỉnh sửa và cam kết bằng tay khi bạn có các tệp mới mà bạn muốn bỏ qua. .gitignoretệp chứa các mẫu được so khớp với tên tập tin trong kho của bạn để xác định có nên bỏ qua các tệp này hay không.
5. Cách tạo repository và cách viết file readme.md trên github
- Repository (kho chứa) nghĩa là nơi mà bạn sẽ lưu trữ mã nguồn và một người khác có thể sao chép (clone) lại mã nguồn đó nhằm làm việc. Repository có hai loại là Local Repository (Kho chứa trên máy cá nhân) và Remote Repository (Kho chứa trên một máy chủ từ xa).
- Cách tạo reppository trên github:
  + Trước tiên bạn cần đăng nhập vào Github, sau đó ấn vào dấu + trên menu và chọn New repository.
		https://imgur.com/a/TNrks
  + Bạn sẽ cần đặt tên cho kho chứa của bạn. Bạn có thể chọn loại kho chứa là Public (ai cũng có thể clone) và Private (chỉ có những người được cấp quyền mới có thể clone).
         	https://imgur.com/a/Z4hdh
  + Khi tạo xong nó sẽ dẫn bạn tới trang hướng dẫn làm việc với kho chứa vừa tạo. Và kho chứa của bạn bây giờ sẽ có địa chỉ là https://github.com/$user-name/$repository, ví dụ https://github.com/PhamHanh96/Hanh.git
  + Việc của bạn bây giờ là hãy clone cái kho chứa này về máy của mình bằng lệnh git clone địa_chỉ
		vd: git clone https://github.com/PhamHanh96/Hanh.git
  
>>>>>>> 73a5e0748d9d47a4b0df84800c6c436f6cdffb33
=======
       Cú pháp: git commit -m "Ghi chú Commit"
  
  + Thay đổi của bạn hiện đang nằm tại HEAD của bản sao cục bộ đang làm việc. Để gửi những thay đổi đó đến repository remote, bạn thực thi
      Cú pháp : git push origin master
    Thay đổi master bằng bất cứ nhánh nào mà bạn muốn đầy những thay đổi đến.
    Nếu bạn chưa clone một repository hiện có và muốn kết nối repository của bạn đến máy chủ remote, bạn phải thêm nó với
     Cú pháp: git remote add origin <máy-chủ>
    Bây giờ bạn đã có thể đẩy các thay đổi của mình vào máy chủ đã chọn
  + Các nhánh (branches) được dùng để phát triển tính năng tách riêng ra từ những nhánh khác. Nhánh master là nhánh "mặc định" khi bạn tạo một repository. Sử dụng các nhánh khác tri đang trong giai đoạn phát triển và merge trở lại nhánh master một khi đã hoàn tất.
    https://imgur.com/a/fVBwJ
    - Tạo một nhánh mới và đặt tên là "dev" và chuyển qua nhánh đó (từ master) bằng cách 
     Cú pháp: git checkout -b dev
    - Trở lại nhánh master
     Cú pháp: git checkout master
    - Và xóa nhánh dev đó lần nửa
     Cú pháp: git branch -d dev
    - Một nhánh không có giá trị với các nhánh khác trừ khi bạn đẩy nhánh đó đến remote repository
     Cú pháp: git push origin <nhánh>
  + Cập nhật và trộn (update & merge)
    - Để cập nhật repository cục bộ của bạn và commit mới nhất, thực thi
       Cú pháp: git pull
      trong thự mục đang làm việc để lấy về (fetch) và trộn (merge) các thay đổi ở remote.
    - Để trộn một nhánh khác vào nhánh đang hoạt động (vd: master), sử dụng
       Cú pháp: git merge <nhánh>
    - Trong cả hai trường hợp, git cố gắng trộn tự động (auto-merge) các thay đổi. Không may, điều này không phải lúc nào cũng làm được và thường dẫn đến xung đột. Trách nhiệm của bạn là trộn các xung đột đó thủ công bằng cách chỉnh sửa các tập tin được hiển thị bởi git. Sau khi thay đổi, bạn phải đánh dấu chúng là đã được trộn (merged) với lệnh
       Cú pháp: git add <tên-tập-tin>
    - Trước khi trộn các thay đổi, bạn có thể xem trước chúng bằng cách
       Cú pháp: git diff <nhánh_nguồn> <nhánh_mục_tiêu>
  + Thay thế các thay đổi cục bộ 
    - Trong trường hợp bạn làm sai điều gì đó, bạn có thể thay thế các thay đổi cục bộ bằng lệnh 
       Cú pháp: git checkout -- <tên-tập-tin>
      Lệnh này thay thế những thay đổi trong "tree" đang làm việc với nội dung mới nhất của HEAD. Các thay đổi đã được thêm vào chỉ mục, kể cả các tập tin mới, điều này sẽ được giữ lại.
    



    
    
>>>>>>> Chinh
