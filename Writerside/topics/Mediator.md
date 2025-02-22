# Mediator

## Giới thiệu

Mediator Pattern định nghĩa một đối tượng trung gian (mediator) để điều phối tương tác giữa các đối tượng, làm giảm sự phụ thuộc trực tiếp giữa chúng.

## Định nghĩa

Mediator Pattern định nghĩa một đối tượng Mediator đóng vai trò trung gian điều phối giao tiếp giữa các đối tượng, tránh cho chúng phải giao tiếp trực tiếp với nhau.

## Mục đích

- Giảm sự phụ thuộc trực tiếp giữa các đối tượng

- Tách biệt cách các đối tượng giao tiếp với nhau

- Dễ dàng mở rộng và thay đổi cách giao tiếp giữa các lớp

## Đặt vấn đề

Giả sử bạn đang phát triển một ứng dụng nhắn tin với các đối tượng User và ChatRoom. Ban đầu, mỗi User giao tiếp trực tiếp với ChatRoom để gửi tin nhắn.

Sau này, yêu cầu thay đổi là cần kiểm duyệt tin nhắn trước khi gửi đi. Lúc này, mối phụ thuộc trực tiếp giữa các đối tượng dẫn tới khó khăn trong việc thay đổi.

## Giải quyết

Mediator Pattern được áp dụng như sau:

- Định nghĩa một lớp Mediator đóng vai trò trung gian điều phối giữa các User và ChatRoom.

- Các User và ChatRoom không giao tiếp trực tiếp với nhau nữa mà thông qua Mediator.

- Khi có yêu cầu thay đổi, ta chỉ cần sửa đổi bên trong Mediator mà không ảnh hưởng các User và ChatRoom.

![](https://refactoring.guru/images/patterns/diagrams/mediator/structure.png)

## Cấu trúc

Các thành phần chính trong Mediator Pattern:

- Mediator: định nghĩa interface để giao tiếp với các Colleague.

- Colleague: giao tiếp với mediator thay vì giao tiếp trực tiếp với các Colleague khác.

- ConcreteMediator: triển khaiMediator để điều phối các Colleague.

- ConcreteColleague: các lớp cụ thể tương tác với mediator.

## Cách triển khai

Để triển khai Mediator Pattern trong Java, chúng ta có thể:

- Định nghĩa interface Mediator với các phương thức trung gian.

- Các lớp Colleague sẽ giữ một tham chiếu tới Mediator và gọi các phương thức đó thay vì giao tiếp trực tiếp.

- Lớp ConcreteMediator sẽ triển khai và điều phối các interation giữa các Colleague.

## Ví dụ

// Ví dụ triển khai Mediator Pattern với các lớp ChatRoom, User

## So sánh

So với Observer, Mediator tập trung vào việc điều phối giao tiếp giữa các đối tượng, còn Observer tập trung vào mối quan hệ một-nhiều giữa các đối tượng.

## Kết luận

Mediator Pattern hữu ích để giảm sự phụ thuộc trực tiếp giữa các lớp, dễ dàng mở rộng và thay đổi chương trình. Tuy nhiên cũng cần tránh lạm dụng mediator dẫn tới phức tạp hóa code.