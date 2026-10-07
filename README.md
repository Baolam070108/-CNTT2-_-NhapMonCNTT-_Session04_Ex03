1. Tạo thư mục
2. New-Item -ItemType Directory -Path .\Farm-Manager\code\app -Force
New-Item -ItemType Directory -Path .\Farm-Manager\database\db -Force
New-Item -ItemType Directory -Path .\Farm-Manager\logs\guides -Force
2. Tạo file
3. New-Item -ItemType File -Path .\Farm-Manager\code\app\main.py -Force
New-Item -ItemType File -Path .\Farm-Manager\code\app\models.py -Force
New-Item -ItemType File -Path .\Farm-Manager\code\app\utils.py -Force
3. Sao chép logs
4. Copy-Item .\Farm-Manager\logs .\Farm-Manager\logs-backup -Recurse -Force
5. * -Recurse: sao chép cả thư mục con và file bên trong.
* -Force: cho phép tạo/ghi đè khi cần.
* .\: đường dẫn tương đối.
4. Kiểm thử
ls .\Farm-Manager
Cây kết quả:
Farm-Manager
├── code
│   └── app
│       ├── main.py
│       ├── models.py
│       └── utils.py
├── database
│   └── db
├── logs
│   └── guides
└── logs-backup
    └── guides
Vì sao dùng .\?
Để đường dẫn không bị phụ thuộc vào ổ đĩa hoặc tên người dùng cụ thể như C:\Users\..., giúp dễ di chuyển và chạy trên máy khác.


