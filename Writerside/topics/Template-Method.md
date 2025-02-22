# Template Method

## Giới thiệu

Template Method Pattern định nghĩa bố cục của một thuật toán trong một phương thức, nhưng để các bước cụ thể của thuật toán được các lớp con cài đặt lại.

## Định nghĩa

Template Method Pattern định nghĩa khung của một thuật toán trong một phương thức, nhưng cho phép các lớp con ghi đè lại các bước cụ thể của thuật toán đó mà không thay đổi cấu trúc chung.

## Mục đích

- Định nghĩa bố cục chung của một thuật toán.

- Cho phép các lớp con cài đặt lại các bước cụ thể mà không làm thay đổi bố cục.

- Giảm sự lặp lại code giữa các lớp có cùng bố cục thuật toán.

## Đặt vấn đề

Giả sử bạn cần xây dựng một ứng dụng có khả năng xuất dữ liệu ra nhiều định dạng khác nhau (csv, xml, json...).

Các bước xuất dữ liệu đều tương tự nhau, nhưng định dạng output thì khác nhau. Việc copy-paste code sẽ dẫn tới khó khăn trong bảo trì sau này.

## Giải quyết

Template Method được áp dụng như sau:

- Định nghĩa một lớp Abstract chứa phương thức template method định nghĩa bố cục chung của thuật toán.

- Cài đặt các bước trừu tượng trong template method.

- Các lớp con sẽ cài đặt lại các bước trừu tượng này.

![](https://refactoring.guru/images/patterns/diagrams/template-method/structure.png)

## Cấu trúc

Các thành phần chính trong Template Method Pattern:

- AbstractClass: định nghĩa template method và các phương thức trừu tượng.

- ConcreteClass: cài đặt lại các phương thức trừu tượng.

## Cách triển khai

Để triển khai Template Method trong Java, chúng ta có thể:

- Tạo một abstract class khai báo các phương thức trừu tượng.

- Cài đặt một template method sử dụng các phương thức trừu tượng đó.

- Các lớp con sẽ cài đặt lại các phương thức trừu tượng.

## Ví dụ

// Ví dụ Template Method áp dụng cho export dữ liệu có định dạng khác nhau

## So sánh với các Pattern

So với Strategy, Template Method định nghĩa bố cục của thuật toán và gọi các phương thức trừu tượng. Strategy định nghĩa riêng các thuật toán có thể hoán đổi cho nhau.

## Kết luận

Template Method giúp tái sử dụng code và tránh lặp lại phần khung của thuật toán giữa các lớp. Tuy nhiên cần cân nhắc khi sử dụng để tránh phức tạp hóa code.
