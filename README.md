# Đồ án cuối kỳ môn mạng xã hội IS353 nhóm 12.
- Giảng viên hướng dẫn: ThS. Nguyễn Thị Anh Thư
- Danh sách thành viên nhóm:
	+ Phạm Trung Nguyên - 22520983
	+ Vũ Thanh Phong - 22521095
	+ Ngô Phương Quyên - 22521095
	+ Võ Minh Quyền - 22521227
	+ Ngô Thị Như Quỳnh - 22521232
# Cấu trúc của repository:
- data:
	+ train_df.csv: File csv chứa dữ liệu mạng user course để train.
	+ val_df.csv: File csv chứa dữ liệu validation.
	+ test_df.csv: File csv chứa dữ liệu test.							
	+ kg_final.txt: Các cạnh mở rộng để xây dựng dữ liệu mạng.
	+ user_list.txt: Danh sách user và các thuộc tính của user trong đó có thêm thuộc tính nhãn cộng đồng để chạy thuật toán FM
	+ user_list_without_community.txt: Danh sách user và các thuộc tính trong đó không có thuộc tính nhãn cộng đồng
	+ trnMat.pkl, valMat.plk, tstMat.pkl là các file chứa ma trận kề biều diễn mạng dùng để huấn luyện mô hình LightGCL
- demo:
	+ demo_ppt.md: Đường dẫn đến ppt nhóm đã sử dụng trong video demo.
	+ demo_scripts.md: Kịch bản của video demo nhóm đã chuẩn bị.
	+ demo_video_link.md: Đường dẫn đến video demo nhóm đã chuẩn bị.
- notebooks:
	+ prepare_data: 
		* Community_Detection.ipynb: ạo dữ liệu quan hệ giữa user-user, course-course có trọng số và thực hiện phát hiện cộng đồng. 
		* Course_Prepare.ipynb: EDA và clean dữ liệu của course và các file quan hệ liên quan đến course
		* Filter_Data.ipynb: Lọc lấy 5-core cho file quan hệ user-course
		* Create_Course_User_Attributes: Tạo các đặc trưng cho course từ các file quan hệ và thêm đặc trưng giới tính cho user.
	+ FM_With_Community_Tag.ipynb: File notebook huấn luyện mô hình FM khi user có thêm đặc trưng nhãn cộng đồng
	+ FM_Without_Community_Tag.ipynb: File notebook huấn luyện mô hình FM khi user không có đặc trưng nhãn cộng đồng
	+ LightGCL: File notebook huấn luyện mô hình LightGCL
	+ Training_GAT_MultiEdgeType.ipynb: File notebook huấn luyện mô hình GAT với nhiều loại node.
	+ Training_GAT_OneEdgeType.ipynb: File notebook huấn luyện mô hình GAT với ma trận utility matrix.
	
		
- src\model:
	+ FM: thư mục chứa các file để huấn luyện mô hình FM
	+ LightGCL: thư mục chứa các file để huấn luyện mô hình LightGCL
- results: chứa kết quả các thuật toán FM và LightGCL
	+ FM_with_community_tag_result.log: Kết quả khi chạy thuật toán FM khi có đắc trưng nhãn cộng đồng
	+ FM_without_community_tag_result.log: Kết quả khi chạy thuật toán FM khi không có đắc trưng nhãn cộng đồng
	+ LightGCL_result.log: Kết quả khi chạy thuật toán LightGCL
- README.md: Mô tả về dự án của nhóm
