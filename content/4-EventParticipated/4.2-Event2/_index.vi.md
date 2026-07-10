---
title: "Sự kiện 2"
date: 2026-06-27
weight: 2
chapter: false
pre: "  4.2.  "
---

# Báo cáo tổng kết: Workshop "Ứng dụng thực tiễn của trí tuệ nhân tạo (AI) trong hạ tầng đám mây"

## Mục tiêu sự kiện

- Chia sẻ các phương pháp thực tiễn tốt nhất trong thiết kế ứng dụng hiện đại.
- Giới thiệu Domain-Driven Design (DDD) và kiến trúc hướng sự kiện (Event-Driven Architecture).
- Hướng dẫn lựa chọn dịch vụ tính toán (Compute Services) phù hợp.
- Giới thiệu các công cụ AI hỗ trợ toàn bộ vòng đời phát triển phần mềm.

## Diễn giả

- **Jignesh Shah** – Director, Open Source Databases
- **Erica Liu** – Sr. GTM Specialist, AppMod
- **Fabrianne Effendi** – Associate Specialist SA, Serverless, Amazon Web Services

## Nội dung nổi bật

### Những hạn chế của kiến trúc ứng dụng truyền thống

- Chu kỳ phát hành sản phẩm kéo dài dẫn đến mất doanh thu và bỏ lỡ cơ hội kinh doanh.
- Quy trình vận hành thiếu hiệu quả làm giảm năng suất và tăng chi phí.
- Không đáp ứng các yêu cầu bảo mật và tuân thủ, làm tăng nguy cơ mất an toàn thông tin và ảnh hưởng đến uy tín doanh nghiệp.

### Chuyển đổi sang kiến trúc ứng dụng hiện đại – Microservices

Kiến trúc hiện đại chia hệ thống thành các dịch vụ độc lập, giao tiếp với nhau thông qua các sự kiện (Events), dựa trên ba thành phần chính:

- Queue Management (Quản lý hàng đợi) để xử lý các tác vụ bất đồng bộ.
- Caching Strategy (Chiến lược bộ nhớ đệm) nhằm tối ưu hiệu năng.
- Message Handling (Xử lý thông điệp) giúp giao tiếp linh hoạt giữa các dịch vụ.

### Domain-Driven Design (DDD)

- Quy trình gồm bốn bước:
  - Xác định Domain Events.
  - Sắp xếp theo dòng thời gian.
  - Xác định các Actor.
  - Thiết lập Bounded Contexts.
- Phân tích ví dụ hệ thống quản lý nhà sách để minh họa cách áp dụng DDD trong thực tế.
- Giới thiệu bảy mô hình Context Mapping giúp kết nối các Bounded Context.

### Event-Driven Architecture

- Ba mô hình tích hợp:
  - Publish/Subscribe
  - Point-to-Point
  - Streaming
- Các lợi ích chính:
  - Giảm sự phụ thuộc giữa các dịch vụ (Loose Coupling).
  - Dễ mở rộng.
  - Khả năng chịu lỗi cao.
- So sánh giữa giao tiếp đồng bộ (Sync) và bất đồng bộ (Async), đồng thời phân tích ưu và nhược điểm của từng mô hình.

### Sự phát triển của Compute Services

- Mô hình Shared Responsibility từ:
  - EC2
  - ECS
  - Fargate
  - Lambda
- Lợi ích của Serverless:
  - Không cần quản lý máy chủ.
  - Tự động mở rộng.
  - Chỉ trả phí theo mức sử dụng.
- Tiêu chí lựa chọn giữa Functions và Containers.

### Amazon Q Developer

- Hỗ trợ tự động hóa toàn bộ vòng đời phát triển phần mềm (SDLC).
- Chuyển đổi mã nguồn:
  - Nâng cấp Java.
  - Hiện đại hóa ứng dụng .NET.
- AWS Transform hỗ trợ chuyển đổi:
  - VMware.
  - Mainframe.
  - .NET.

# Kiến thức tiếp thu

## Tư duy thiết kế hệ thống

- Luôn bắt đầu từ bài toán nghiệp vụ (Business-first), thay vì bắt đầu từ công nghệ.
- Xây dựng ngôn ngữ chung (Ubiquitous Language) giữa đội ngũ nghiệp vụ và kỹ thuật.
- Phân chia Bounded Context để kiểm soát sự phức tạp của hệ thống.

## Kiến trúc kỹ thuật

- Event Storming là phương pháp trực quan để mô hình hóa quy trình nghiệp vụ.
- Ưu tiên giao tiếp bất đồng bộ thay vì chỉ sử dụng lời gọi đồng bộ.
- Hiểu rõ khi nào nên sử dụng:
  - Sync
  - Async
  - Publish/Subscribe
  - Streaming
- Nắm được tiêu chí lựa chọn giữa VM, Containers và Serverless.

## Chiến lược hiện đại hóa hệ thống

- Thực hiện theo từng giai đoạn với lộ trình rõ ràng.
- Hiểu Framework 7Rs cho các chiến lược hiện đại hóa ứng dụng.
- Đánh giá hiệu quả thông qua ROI thay vì chỉ tập trung vào công nghệ.

## Khả năng áp dụng vào công việc

- Áp dụng DDD vào các dự án thông qua Event Storming.
- Xác định ranh giới Microservices bằng Bounded Context.
- Thay thế một số luồng đồng bộ bằng Event-Driven Architecture.
- Triển khai AWS Lambda cho các chức năng phù hợp.
- Tích hợp Amazon Q Developer vào quy trình phát triển để nâng cao năng suất.

# Trải nghiệm tham dự sự kiện

Tham gia workshop **"GenAI-powered App-DB Modernization"** mang lại cho em nhiều kiến thức thực tế về thiết kế hệ thống hiện đại và quá trình hiện đại hóa ứng dụng.

## Học hỏi từ các diễn giả

Các diễn giả đã chia sẻ nhiều kinh nghiệm thực tiễn trong việc thiết kế và chuyển đổi hệ thống. Tuy nhiên, với một thành viên mới, các khái niệm như Context Mapping trong DDD ban đầu khá khó tiếp cận.

Thông qua các ví dụ thực tế, em nhận ra rằng việc xây dựng hệ thống cần bắt đầu từ bài toán nghiệp vụ (Business-first) và sử dụng một ngôn ngữ thống nhất (Ubiquitous Language), thay vì chỉ tập trung vào việc lập trình.

## Tiếp cận các kỹ thuật mới

Kỹ thuật Event Storming giúp em dễ hình dung cách mô hình hóa các quy trình nghiệp vụ thành các Domain Events.

Ngoài ra, em hiểu rõ hơn sự khác biệt giữa:

- Đồng bộ và bất đồng bộ (Sync vs Async).
- Functions và Containers.

Qua đó nhận thấy việc lựa chọn kiến trúc trong môi trường thực tế cần dựa trên hiệu quả vận hành và ROI thay vì xu hướng công nghệ.

## Trải nghiệm với các công cụ hiện đại

Amazon Q Developer là nội dung tạo ấn tượng mạnh nhất đối với em, đặc biệt là khả năng chuyển đổi mã nguồn và hỗ trợ hiện đại hóa hệ thống cũ.

Là một thành viên mới, việc có AI hỗ trợ trong quá trình phát triển giúp em tự tin hơn khi tiếp cận các dự án lớn.

## Giao lưu và trao đổi

Workshop cũng giúp em quan sát cách các nhóm kỹ thuật và nghiệp vụ phối hợp với nhau trong quá trình phát triển sản phẩm, từ đó hình thành tư duy làm việc chuyên nghiệp hơn.

# Bài học rút ra

- Hiện đại hóa hệ thống cần thực hiện theo từng giai đoạn với lộ trình rõ ràng.
- Cần đánh giá hiệu quả thông qua ROI thay vì chạy theo công nghệ mới.
- AI và các kiến trúc hiện đại giúp giảm sự phụ thuộc giữa các thành phần của hệ thống, đồng thời nâng cao năng suất của cá nhân và nhóm phát triển.

# Một số hình ảnh của sự kiện

<p align="center">
    <img src="1783684021428_2088812899270591419_2174945698042172265_02d3268fd57a8925c2221899ff70d09d.jpg" width="700">
</p>

<p align="center">
    <img src="1783684021503_2088812899270591419_2174945698042172265_02f85b797bf7aa24e4779e4f6073230.jpg" width="700">
</p>

<p align="center">
    <img src="1783684021573_2088812899270591419_2174945698042172265_ac9fba72ece06904661cf4fb68566bbb.jpg" width="700">
</p>

> Overall, although the workshop covered a lot of advanced system architecture concepts that were quite challenging for a beginner, it was a highly rewarding experience. The event gave me a comprehensive overview of the application modernization process, and a clearer understanding of both my learning roadmap and practical approaches to software system design.