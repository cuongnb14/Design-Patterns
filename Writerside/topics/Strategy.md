# Strategy

## Giới thiệu

Strategy Pattern định nghĩa một nhóm các thuật toán có thể hoán đổi cho nhau để thay đổi thuật toán bên trong một đối tượng tại runtime.

## Định nghĩa

Strategy Pattern định nghĩa tập hợp các thuật toán có thể thay thế cho nhau và cung cấp cách để client có thể dễ dàng thay đổi các thuật toán này độc lập với ngữ cảnh sử dụng.

## Mục đích

- Tách biệt thuật toán riêng lẻ thành các lớp độc lập.

- Các thuật toán có thể hoán đổi cho nhau dễ dàng.

- Tránh sử dụng các câu lệnh điều kiện phức tạp.

## Đặt vấn đề

Giả sử bạn đang phát triển một game, có lớp NhânVật có phương thức diChuyển(). Ban đầu chỉ có cách di chuyển bằng đi bộ. Sau này có thêm yêu cầu bay và bơi.

Nếu đặt tất cả các cách di chuyển vào lớp NhânVật sẽ dẫn đến lớp này bị phình to, khó bảo trì.

Làm thế nào để dễ dàng thêm mới cách di chuyển mà không ảnh hưởng đến lớp NhânVật?

## Giải quyết

Strategy Pattern được áp dụng như sau:

- Mỗi thuật toán di chuyển được đóng gói thành một lớp riêng biệt, triển khai từ một interface.

- Lớp NhânVật sẽ lưu trữ một tham chiếu tới interface di chuyển.

- Khi cần thay đổi thuật toán, chỉ cần gán lớp triển khai mới cho tham chiếu đó.

![](https://refactoring.guru/images/patterns/diagrams/strategy/structure.png)

## Cấu trúc

Các thành phần chính trong Strategy Pattern:

- Strategy: interface chung cho các thuật toán.

- ConcreteStrategy: các lớp triển khai cụ thể các thuật toán.

- Context: lớp sử dụng các thuật toán thông qua Strategy.

## Cách triển khai

Để triển khai Strategy Pattern trong Java, chúng ta có thể:

- Định nghĩa một interface chung cho Strategy.

- Các ConcreteStrategy triển khai interface đó.

- Context sẽ có một tham chiếu tới Strategy và sử dụng nó.

## Ví dụ

// Ví dụ minh họa Strategy Pattern áp dụng cho cách di chuyển của nhân vật

## So sánh với các Pattern

So với State, Strategy tập trung vào việc thay đổi riêng lẻ một thuật toán cụ thể, còn State tập trung vào việc thay đổi toàn bộ hành vi dựa trên trạng thái.

## Kết luận

Strategy Pattern giúp tách biệt các thuật toán riêng lẻ thành các lớp độc lập, dễ dàng thay đổi và mở rộng. Tuy nhiên cũng cần tránh lạm dụng dẫn đến phức tạp code.