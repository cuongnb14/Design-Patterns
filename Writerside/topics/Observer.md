# Observer

## Giới thiệu

Observer Pattern định nghĩa mối phụ thuộc một-nhiều giữa các đối tượng để khi một đối tượng thay đổi trạng thái, các đối tượng phụ thuộc vào nó sẽ được thông báo và cập nhật.

## Định nghĩa

Observer Pattern mô tả mối quan hệ giữa các đối tượng theo mô hình phát trực tiếp (publish-subscribe), trong đó có một đối tượng (subject) sẽ "báo cáo" sự thay đổi trạng thái của nó tới các đối tượng đăng ký quan sát (observer) để chúng cập nhật.

## Mục đích

- Định nghĩa mối phụ thuộc một-nhiều giữa các đối tượng.

- Khi một đối tượng thay đổi trạng thái, tất cả các đối tượng phụ thuộc vào nó sẽ được thông báo và cập nhật.

## Đặt vấn đề

Giả sử bạn đang phát triển một website thương mại điện tử với các chức năng sau:

- Người dùng có thể đăng ký nhận thông báo khi một sản phẩm nào đó có giá giảm.

- Khi giá sản phẩm thay đổi, tất cả người dùng đã đăng ký sẽ nhận được thông báo.

Làm thế nào để triển khai khi có hàng triệu người dùng cùng theo dõi hàng triệu sản phẩm khác nhau?

## Giải quyết

Observer Pattern được áp dụng như sau:

- Định nghĩa một Subject (đối tượng chủ đề) đại diện cho sản phẩm.

- Người dùng (Observer) có thể đăng ký theo dõi Subject.

- Khi trạng thái của Subject thay đổi (giá sản phẩm) thì sẽ thông báo tới tất cả Observer đã đăng ký.

![](https://refactoring.guru/images/patterns/diagrams/observer/structure.png)

## Cấu trúc

Các thành phần trong Observer Pattern:

- Subject: đối tượng chủ thể cần theo dõi. Nó duy trì danh sách các Observer và thông báo cho chúng khi trạng thái thay đổi.

- Observer: đối tượng quan sát Subject. Nó đăng ký theo dõi Subject và cập nhật khi nhận được thông báo từ Subject.

- ConcreteSubject và ConcreteObserver: các cài đặt cụ thể.

## Cách triển khai

Để triển khai Observer Pattern trong Java, có thể:

- Sử dụng interface java.util.Observable và java.util.Observer.
- Tự định nghĩa Subject, Observer interface và các cài đặt tương ứng.

## Ví dụ

// Ví dụ đăng ký nhận thông báo khi giá sản phẩm thay đổi

## So sánh

So với PubSub, Observer tập trung vào mối quan hệ giữa các object, còn PubSub tập trung vào việc truyền thông điệp.

## Kết luận

Observer Pattern thích hợp để xây dựng các chức năng thông báo sự kiện trong hệ thống. Tuy nhiên cũng cần tránh lạm dụng và làm phức tạp hóa code.