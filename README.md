<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Thiệp Cho Em</title>
    <style>
        body {
            margin: 0;
            overflow: hidden;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #FFC0CB; /* Màu hồng nhẹ */
            transition: background-color 0.5s;
            text-align: center;
        }
        .card {
            font-size: 24px;
            font-family: "Arial", sans-serif;
            color: #4A148C;
            font-weight: bold;
            padding: 20px;
            background: white;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            max-width: 80%;
            text-align: center;
            transition: opacity 0.5s;
        }
    </style>
</head>
<body>

    <div class="card">💌 Chạm vào màn hình để bắt đầu!</div>

    <script>
        // Danh sách nội dung tin nhắn
        const messages = [
            "Chào em",
            "Cứ mỗi lần anh thấy mình không ngu hơn được nữa rồi",
            "Thì anh lại làm một việc còn ngu hơn",
            "Anh xin lỗi em",
            "Em là tuyệt vời nhất trong mắt anh TT",
            "Chúc em ngày mới tốt lành"
        ];

        // Danh sách màu nền để thay đổi theo từng câu
        const colors = ["#FFC0CB", "#FFD700", "#ADD8E6", "#FF6347", "#90EE90", "#D8BFD8"];

        let index = 0; // Vị trí nội dung hiện tại

        document.body.addEventListener("touchstart", function () {
            index = (index + 1) % messages.length; // Chuyển sang nội dung tiếp theo
            document.querySelector(".card").innerHTML = messages[index]; // Cập nhật nội dung
            document.body.style.backgroundColor = colors[index]; // Đổi màu nền
        });
    </script>

</body>
</html>
