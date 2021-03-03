Phân tích website setsail page Winter

+ Nguyên tắc và các bước thực hiện.
1.vị trí
2.kích thước
3.màu sắc
4.kiển dáng

nguyên tăc:
  - từ ngoài vào trong , 
   -từ trên xuống dưới
=> từ tổng quan đến chi tiết









1.Phân tích ------->> ok
  1.header  ------> ok
  2.slider big ------------> ok
  3.slider smooth smaller  ---------> ok còn js
  4.video review tour  ----> ok
  5.top review with slider small ----> chua js
  6.service  -----> ok 
  7.total tour (slider image) --> ok
  8.country tour
  9. footer
2.Xây móng

3.Xây dựng từng phần theo phân tích
4.hoàn thiện
 

############################-------> còn lại phần footer

lỗi: thanh next và prev ở big header không thể hover.



 ------------------------------ practice -----------
 ## Để tạo hiệu ứng hover border ở chân của text chạy ta làm như sau
   +  thứ nhất 
    ta tạo một lớp giả cho class cần tạo hover gạch chấn
    sau đó xét chiều cao cho nó, và để width: 0;
       đổ background-color: là màu cần hover,
   + Sau khi hover vào thì để width: 100%;
     để tạo hiệu ứng chạy ta dùng transiton cho chiều width và để thời gian (  transition: width 0.3s ) -> thì phần background
     của lớp giả sẽ phóng ra
      và muốn có hiệu ứng thu vào thì cũng cho thời gian của width ở class gốc là được

   ####  để tạo hiệu ứng hover zoom ảnh ta dùng thuộc tính :
          transition: transform 0.3s; ở class của image , đặt kích thước cho imge,
          sau đó ở hover ta cho thuộc tính transform: scale(1.2); là được (chưa có cách hay hơn)

   ####  để tạo xem video với javascript thì đầu tiên
    + ta lấy id của các thẻ để xem và dừng video
      after that ta tạo function để thực thi dừng và mở video và để sự kiện onclick(nameFunction()) vào thẻ video
      nếu dừng video thì ta để display = none;
    ((((((((((((((((((
     var videoPlayer = document.getElementById("videoPlayer");
    var myVideo = document.getElementById("myVideo");
    var videoModal = document.getElementById("videoModal");

    function stopVideo(){
        videoPlayer.style.display = 'none';
        videoModal.style.display = 'none';
        myVideo.pause();
    }
    function playVideo(file){
        myVideo.src = file;
        myVideo.autoplay = true;
        videoModal.style.display = 'block';
        videoPlayer.style.display = 'block';
    } 
    ))))))))))))))))))

    ##### ta có thể dùng transition cho màu săc để hiệu ứng
      transition: color 0.2s ease;
