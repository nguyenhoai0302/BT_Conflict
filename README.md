NHỮNG ĐIỀU CẦN LƯU Ý

1. Nguyên tắc khi lằm việc nhóm
- Tạo hai nhánh chính: 
    - Main Branch (main hoặc master): Đây là nhánh chính của dự án, chứa code đã qua kiểm thử và sẵn sàng cho sản phẩm. Mọi PR chỉ được merge vào nhánh này sau khi đã review và test cẩn thận. Thành viên không được phép push code trực tiếp vào nhánh này. Code chỉ được merge thông qua pull request sau khi review.
    - Development Branch (dev or develop): Đây là nhánh dùng để code chính, nơi các thành viên làm việc với các tính năng mới, sửa lỗi, hoặc các cải tiến. Tất cả công việc sẽ được thực hiện trên các nhánh con từ dev, và sau đó tạo PR để merge vào dev.
    - Lưu ý: 
- Cách tạo Pull Requets (PR):
    - Feature Branch: Khi bắt đầu làm việc trên một tính năng mới hoặc sửa lỗi, mỗi developer tạo một nhánh riêng từ dev.
    Ví dụ: feature/add-login.
    - Pull Request vào dev: Sau khi hoàn thành, developer sẽ tạo pull request từ nhánh feature vào nhánh dev. Khi tạo pull request cần bào cho người revew code để merge or trong lúc tạo pull requets thì assign họ vào luôn. 
    - Pull Request vào main: Khi nhánh dev đã ổn định và đảm bảo đã hoàn tất các tính năng, PR sẽ được tạo từ dev vào main. Đây là bước cuối cùng trước khi đưa sản phẩm vào sử dụng chính thức.

- Phân công người review code và merge code: Trong nhóm sẽ chỉ định ra một người là người review code và merge code khi các thành viên đã làm xong chức năng của mình. Người này có nhiệm vụ kiểm tra code, đảm bảo chất lượng, kiểm tra logic, coding convention và tính ổn định của chức năng mới sau khi thấy code đã ổn thì tiến hành merge vào nhánh develop.

2. Nguyên tắc đặt tên Nhánh
- Tên nhánh rõ ràng, mô tả chính xác: Tên nhánh cần ngắn gọn nhưng đủ thông tin để biết mục đích của nhánh.
Ví dụ: feature/add-login, bugfix/fix-header.
- Sử dụng tiền tố hợp như feature/, bugfix/, hotfix/, chore/ để phân loại các nhánh.
- Không sử dụng ký tự đặc biệt: Tránh các ký tự như dấu cách, ký tự đặc biệt không được phép trong Git.
- Chỉ dùng dấu gạch ngang "-" hoặc gạch chéo "/".

3. Nguyên tắc khi code 
- Viết code sạch và dễ đọc: Tuân theo chuẩn code style (coding conventions) của dự án để tất cả mọi người đều dễ hiểu và quản lý.
- Sử dụng tên biến và hàm có ý nghĩa: Tên biến, hàm cần thể hiện rõ mục đích sử dụng, tránh những tên chung chung như data1, temp.
Ví dụ:  

- Giữ code ngắn gọn và đơn giản: Tránh lặp lại code, sử dụng các phương pháp tổ chức và tái sử dụng code để dễ dàng bảo trì.
- Bình luận đúng chỗ: Chỉ bình luận ở những đoạn code khó hiểu hoặc có logic phức tạp, không cần bình luận quá mức.
- Test kỹ lưỡng: Đảm bảo rằng code mới không làm hỏng các chức năng hiện tại, viết unit tests nếu cần thiết.

4. Lưu ý khi giải quyết conflict
- Kiểm tra nguyên nhân của conflict: Trước khi sửa, cần hiểu rõ tại sao conflict xảy ra để có thể giải quyết hợp lý.
- Liên lạc với thành viên có liên quan: Nếu không rõ cách giải quyết hoặc cần thêm thông tin, hãy trao đổi với người có liên quan để tìm ra phương án tốt nhất.
- Test sau khi merge: Sau khi giải quyết conflict và thực hiện merge, cần test tất cả các chức năng lại để đảm bảo không có lỗi phát sinh hoặc làm mất code.