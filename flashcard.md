#flashcards 
> Docker là gì::Một nền tảng giúp đóng gói, phân phối và chạy ứng dụng trong các container.
<!--SR:!2025-03-29,2,248-->

> Docker container là gì::Một đơn vị phần mềm nhẹ, độc lập, chứa mọi thứ cần thiết để chạy một ứng dụng (code, runtime, system tools, libraries, etc.)
<!--SR:!2025-03-29,2,248-->

> Docker image là gì::Một bản mẫu chỉ đọc dùng để tạo Docker container.
<!--SR:!2025-03-29,2,248-->

> Dockerfile dùng để làm gì::Dùng để định nghĩa cách tạo Docker image.
<!--SR:!2025-03-29,2,248-->

> Dockerfile gồm các lệnh cơ bản nào:::FROM, RUN, COPY, CMD
<!--SR:!2025-03-29,2,248!2025-03-29,2,248-->

> Lệnh `docker build` dùng để làm gì
> ?
> Dùng để tạo image từ Dockerfile
<!--SR:!2025-03-29,2,248-->

> Lệnh `docker run`
> ?
> Dùng để tạo và chạy container từ image
<!--SR:!2025-03-29,2,248-->

> `docker ps -a`::Liệt kê tất cả các container, kể cả đang dừng
<!--SR:!2025-03-29,2,248-->

> Câu lệnh để xóa container::`docker rm <container_id>`
<!--SR:!2025-03-29,2,248-->

> Câu lệnh để xóa image::`docker rmi <image_id>`
<!--SR:!2025-03-29,2,248-->

> Volume là gì:::Là cơ chế dùng để lưu trữ dữ liệu ngoài container
<!--SR:!2025-03-29,2,248!2025-03-29,2,248-->

> Bind mount là gì:::Là cách mount thư mục từ máy host vào container
<!--SR:!2025-03-29,2,248!2025-03-29,2,248-->

> Sự khác nhau giữa Volume và Bind mount
> ?
> Volume do Docker quản lý, an toàn và linh hoạt hơn; Bind mount dùng thư mục cụ thể trên host
<!--SR:!2025-03-29,2,248-->

> Docker Compose là gì
> ??
> Công cụ định nghĩa và chạy multi-container ứng dụng Docker với file YAML
<!--SR:!2025-03-29,2,248!2025-03-29,2,248-->

> File mặc định của Docker Compose::`docker-compose.yml`
<!--SR:!2025-03-29,2,248-->

> `docker-compose up -d` dùng để làm gì::Khởi chạy các container trong background theo file docker-compose.yml
<!--SR:!2025-03-29,2,248-->

> Docker Hub là gì:::Là registry nơi lưu trữ và chia sẻ Docker image
<!--SR:!2025-03-29,2,248!2025-03-29,2,248-->

> Docker network là gì:::Là cơ chế cho phép các container giao tiếp với nhau và với bên ngoài
<!--SR:!2025-03-29,2,248!2025-03-29,2,248-->

> Bridge network trong Docker
> ?
> Kiểu mạng mặc định cho container, cho phép các container giao tiếp nội bộ với nhau
<!--SR:!2025-03-29,2,248-->

> Lệnh để vào bên trong container đang chạy
> ??
> `docker exec -it <container_id> /bin/bash`
<!--SR:!2025-03-29,2,248!2025-03-29,2,248-->

> Multi-stage build là gì:::Giúp tạo image nhẹ hơn bằng cách chia các bước build thành nhiều stage
<!--SR:!2025-03-29,2,248!2025-03-29,2,248-->

> Docker Swarm là gì:::Công cụ quản lý nhiều Docker host thành một cluster
<!--SR:!2025-03-29,2,248!2025-03-29,2,248-->

> So sánh Docker Swarm và Kubernetes
> ?
> Swarm dễ thiết lập hơn, phù hợp cho project nhỏ; Kubernetes mạnh mẽ, phức tạp, dùng cho hệ thống lớn
<!--SR:!2025-03-29,2,248-->

> Docker networking là gì:::Là cơ chế cho phép container giao tiếp với nhau hoặc với bên ngoài
<!--SR:!2025-03-29,2,248!2025-03-29,2,248-->

> Các kiểu network mặc định của Docker
> ?
> bridge, host, none, overlay
<!--SR:!2025-03-29,2,248-->

> Overlay network là gì:::Cho phép container trên nhiều host giao tiếp với nhau
<!--SR:!2025-03-29,2,248!2025-03-29,2,248-->

> `host network` là gì:::Dùng chung network stack với host, không bị NAT
<!--SR:!2025-03-29,2,248!2025-03-29,2,248-->

> Lệnh tạo custom bridge network
> ??
> `docker network create --driver bridge my-network`
<!--SR:!2025-03-29,2,248!2025-03-29,2,248-->

> Port mapping là gì:::Là ánh xạ cổng của host với container (ví dụ: -p 8080:80)
<!--SR:!2025-03-29,2,248!2025-03-29,2,248-->

> Tại sao nên hạn chế dùng root user trong container
> ?
> Vì tăng rủi ro bảo mật nếu container bị xâm nhập
<!--SR:!2025-03-29,2,248-->

> Docker Security Best Practices::dùng image chính thức, cập nhật thường xuyên, không chạy bằng root, scan image trước khi dùng
<!--SR:!2025-03-29,2,248-->

> Docker scan là gì:::Công cụ kiểm tra lỗ hổng bảo mật trong image
<!--SR:!2025-03-29,2,248!2025-03-29,2,248-->

> Lệnh quét lỗ hổng bảo mật với Docker CLI  
>??  
> `docker scan <image_name>`

> Multi-stage build giúp tối ưu Dockerfile như thế nào
> ?
> Giảm kích thước image bằng cách chỉ giữ lại stage cuối cùng cần thiết để chạy app
<!--SR:!2025-03-29,2,248-->

> Layer caching là gì:::Cơ chế tăng tốc độ build bằng cách tái sử dụng các layer không đổi
<!--SR:!2025-03-29,2,248!2025-03-29,2,248-->

> `COPY` vs `ADD` trong Dockerfile:::COPY đơn giản và rõ ràng, ADD có thêm tính năng như giải nén file
<!--SR:!2025-03-29,2,248!2025-03-29,2,248-->

> Lý do nên đưa các lệnh cài đặt dependencies lên đầu Dockerfile
> ?
> Để tận dụng layer cache, tránh build lại khi chỉ thay đổi code
<!--SR:!2025-03-29,2,248-->

> .dockerignore để làm gì:::Để loại trừ file/thư mục không cần thiết khỏi context build
<!--SR:!2025-03-29,2,248!2025-03-29,2,248-->

> Pipeline CI/CD thường dùng Docker để làm gì
> ??
> Đóng gói ứng dụng, kiểm thử, và deploy tự động trong môi trường nhất quán
<!--SR:!2025-03-29,2,248!2025-03-29,2,248-->

> Docker in CI/CD là gì:::Giúp đảm bảo môi trường build/test giống môi trường production
<!--SR:!2025-03-29,2,248!2025-03-29,2,248-->

> `docker-compose -f docker-compose.test.yml up` dùng để làm gì::Chạy testing environment bằng Docker Compose
<!--SR:!2025-03-29,2,248-->

> Kết hợp Docker với GitHub Actions
> ?
> Dùng Docker để build, test và deploy ứng dụng tự động mỗi lần push code
<!--SR:!2025-03-29,2,248-->

> Kubernetes là gì:::Là nền tảng điều phối container giúp triển khai, mở rộng và quản lý ứng dụng
<!--SR:!2025-03-29,2,248!2025-03-29,2,248-->

> Pod là gì:::Đơn vị triển khai nhỏ nhất trong Kubernetes, có thể chứa một hoặc nhiều container
<!--SR:!2025-03-29,2,248!2025-03-29,2,248-->

> Tại sao cần Docker trong Kubernetes
> ?
> Docker giúp đóng gói ứng dụng, còn Kubernetes giúp quản lý, triển khai, scale và giám sát các container đó
<!--SR:!2025-03-29,2,248-->

> Kubelet là gì:::Là thành phần chạy trên mỗi node, giao tiếp với Docker để quản lý container
<!--SR:!2025-03-29,2,248!2025-03-29,2,248-->

> Kubernetes dùng gì để thay thế Docker từ phiên bản mới
> ??
> Containerd hoặc CRI-O (thông qua Container Runtime Interface)
<!--SR:!2025-03-29,2,248!2025-03-29,2,248-->

> Deployment trong Kubernetes là gì:::Là cách triển khai và quản lý bản sao (replica) của Pod
<!--SR:!2025-03-29,2,248!2025-03-29,2,248-->

> Sự khác biệt giữa Pod và Container trong Kubernetes
> ?
> Pod là một lớp trừu tượng chứa container, cung cấp môi trường chạy container có mạng và lưu trữ riêng
<!--SR:!2025-03-29,2,248-->

> Helm là gì:::Là công cụ quản lý package (chart) cho ứng dụng trong Kubernetes
<!--SR:!2025-03-29,2,248!2025-03-29,2,248-->

> Lệnh chuyển đổi Docker image thành Kubernetes YAML
> ??
> `kompose convert`
<!--SR:!2025-03-29,2,248!2025-03-29,2,248-->

> Best Practices khi dùng Docker gồm:
> ??
> - Dùng image nhẹ (alpine, slim)
> - Tối ưu Dockerfile để giảm layer
> - Không hardcode thông tin nhạy cảm
> - Sử dụng `.dockerignore` đầy đủ
> - Gắn tag rõ ràng cho image
<!--SR:!2025-03-29,2,248!2025-03-29,2,248-->


> Lý do không nên dùng `latest` tag trong production
> ??
> Vì không xác định được phiên bản cụ thể, gây lỗi không lường trước khi image thay đổi
<!--SR:!2025-03-29,2,248!2025-03-29,2,248-->

> Multi-stage builds giúp gì:::Tách biệt quá trình build và runtime
<!--SR:!2025-03-29,2,248!2025-03-29,2,248-->

> Lệnh kiểm tra kích thước image Docker
> ??
> `docker images`
<!--SR:!2025-03-29,2,248!2025-03-29,2,248-->

> Immutable Infrastructure là gì:::Nguyên tắc không chỉnh sửa container khi đang chạy, thay vào đó tái build & redeploy
<!--SR:!2025-03-29,2,248!2025-03-29,2,248-->

> Cách kiểm soát version image trong production
>?
> Gắn tag version cụ thể (ví dụ: myapp:1.2.3)
<!--SR:!2025-03-29,2,248-->

