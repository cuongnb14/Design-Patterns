# Visitor

## Giới thiệu

Visitor Pattern cho phép thêm các thao tác mới vào cấu trúc đối tượng hiện có mà không cần thay đổi code.

## Định nghĩa

Visitor Pattern tách biệt các thao tác cần thực hiện lên các đối tượng khỏi các đối tượng đó, bằng cách đưa logic vào một lớp Visitor riêng biệt.

## Mục đích

- Cho phép thêm các thao tác mới lên cấu trúc đối tượng hiện có mà không cần thay đổi code.

- Tách biệt các thao tác khỏi các đối tượng thực hiện chúng.

## Đặt vấn đề

Giả sử bạn có một cấu trúc cây đối tượng phức tạp đại diện cho một tài liệu. Bây giờ cần thêm chức năng xuất tài liệu ra nhiều định dạng khác nhau (json, xml, pdf...).

Làm thế nào để thêm chức năng mới mà không làm ảnh hưởng đến cấu trúc cây đối tượng hiện tại?

## Giải quyết

Visitor Pattern được áp dụng như sau:

- Định nghĩa một interface Visitor với các phương thức visit tương ứng với từng lớp Element.

- Các lớp Element sẽ có phương thức accept nhận vào một Visitor.

- Tạo các ConcreteVisitor triển khai các phương thức visit để thực hiện các thao tác cụ thể lên Element.

![](https://refactoring.guru/images/patterns/diagrams/visitor/structure.png)

## Cấu trúc

Các thành phần chính trong Visitor Pattern:

- Visitor: định nghĩa các phương thức thao tác trên các Element.

- ConcreteVisitor: triển khai các phương thức trên.

- Element: định nghĩa phương thức accept nhận vào một Visitor.

- ConcreteElement: các lớp cụ thể cần áp dụng thao tác.

## Cách triển khai

Để triển khai Visitor trong Java, ta có thể:

- Định nghĩa interface Visitor với các phương thức visit tương ứng với từng Element.

- Các Element có phương thức accept nhận vào một Visitor.

- Các ConcreteVisitor triển khai các phương thức visit.

## Ví dụ

// Ví dụ minh họa Visitor Pattern áp dụng cho việc xuất tài liệu

## So sánh với các Pattern

So với Strategy, Visitor tách logic ra khỏi các đối tượng, trong khi Strategy nhóm các thuật toán lại với nhau.

## Kết luận

Visitor Pattern giúp tách rời các thao tác khỏi các đối tượng thực thi, giúp dễ dàng bảo trì và mở rộng. Tuy nhiên cũng cần cân nhắc để tránh lạm dụng dẫn đến phức tạp code.