# sql-co-ban
Tổng hợp một số câu lệnh SQL cơ bản
#CHỐNG TRÙNG LẶP

{SELECT DISTINCT MASP FROM HOADONCHITIET}

-- Lấy top
SELECT TOP 1 WITH TIES ....
-- LẤY THÔNG TIN TRONG KHOẢNG
SELECT * FROM NHANVIEN WHERE LUONG >=100 AND LUONG <= 300

SELECT * FROM NHANVIEN WHERE LUONG BETWEEN 100 AND 300

-- LẤY THÔNG TIN CÓ LÀ NULL
SELECT * FROM NHANVIEN WHERE DIENTHOAI IS NULL

-- LẤY THÔNG TIN NHÂN VIÊN CÓ CÁC MÃ SF001, SF005, SF009
SELECT * FROM NHANVIEN WHERE MANV IN('SF001','SF005','SF009');

-- LÀM VIỆC VỚI CÁC HÀM SỐ HỌC
-- LÀM TRÒN SỐ
SELECT ROUND(3.456,2)
-- LẤY CẬN TRÊN ( LÀM TRÒN LÊN)
SELECT CEILING(3.456);
-- LẤY CẬN DƯỚI ( LÀM TRÒN XUỐNG)
SELECT FLOOR(3.456)
-- LẤY SỐ MŨ
SELECT POWER (2,3)
-- LẤY CĂN BẬC HAI
SELECT SQRT(9) AS CANBAC2

-- LÀM VIỆC VỚI CÁC HÀM KÝ TỰ
-- HÀM CHUYỂN VỀ CHỮ THƯỜNG
SELECT LOWER(N' Lập Trinh')
-- HÀM CHUYỂN VỀ CHỮ HOA
SELECT UPPER(N' Lập Trinh')
-- HÀM THAY THẾ CHUỖI
SELECT REPLACE (' Lap Trinh A','A','c');

-- LÀM VIỆC VỚI NGÀY THÁNG
-- LẤY NGÀY GIỜ HIỆN TẠI
SELECT GETDATE();
-- LẤY THÔNG TIN NGÀY, THÁNG, NĂM
SELECT DAY(GETDATE()) NGAY, MONTH(GETDATE()) THANG, YEAR(GETDATE()) NAM
-- LAY THONG TIN DE BIET THANG SAU CỦA NGÀY NÀY
SELECT DATEADD(M,1,GETDATE());
-- SO SÁNH HAI NGÀY ( ĐẾM SỐ NGÀY TRONG KHOẢNG )
SELECT DATEDIFF(D,'06/05/2016','06/10/2016') AS SONGAY;
-- CHUYỂN TỪ DẠNG CHUỖI SANG SỐ
SELECT CAST('03' AS INT ) *2;
-- CHUYỂN CHUỖI RA NGÀY THÁNG
SELECT CONVERT(DATE, '2/05/2017',103) -- 103 = NGÀY TRƯỚC THÁNG SAU, 101 = THÁNG TRƯỚC NGÀY SAU
 

