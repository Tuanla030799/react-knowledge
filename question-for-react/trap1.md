### 1. Rect là gì ? tại sao sử dụng nó ?
  - nó cung cấp các components dễ dàng chia sẻ các phần dao diện của người dùng(UI), ddiiefu mà bản thân HTML không thể làm được

### 2. JSX là gì ?
  - nếu bạn viết một 'div' trong JSX thì nó sẽ <=> với việc gọi 'React.createElement()' qua đó bạn có thể rút gọn cú pháp khi sd JSX

### 3. Có 2 cách truyền data cho các react component
  - props
  ![props](https://scontent.fhan3-5.fna.fbcdn.net/v/t39.30808-6/291686476_580326946827865_869158144550169769_n.jpg?_nc_cat=109&ccb=1-7&_nc_sid=5cd70e&_nc_ohc=sNN32AtAvwoAX9HXmZk&_nc_ht=scontent.fhan3-5.fna&oh=00_AT8mN77S4BGwF5aHRf15CPTdHfVYHqj7FyPRYFB0of62wQ&oe=62E46098)
  - context api
  ![context](https://scontent.fhan3-2.fna.fbcdn.net/v/t39.30808-6/291791913_580326906827869_6167857080590780628_n.jpg?_nc_cat=101&ccb=1-7&_nc_sid=5cd70e&_nc_ohc=iAaFsPVfTBMAX-jgp20&_nc_ht=scontent.fhan3-2.fna&oh=00_AT9NuXDoqy2RS2Y7yvUwiAg94mdtOv_nn4ejMuIXCl5DaQ&oe=62E3686C)  

### 4. Sự khác nhau giữa State và props là gì ?
  - bạn có thể hiểu đơn giản rẳng props là những tham số của một hàm mà tồn tại bên ngoài component. Trong khi state là các giá trị thay đổi theo thời gian, được khai báo và chỉ tồn tại bên trong component

### 5. React fragments dùng để làm gì ?
  - cú pháp của fragments như sau : <></>, đôi khi ta cần bỏ nhiều react element dưới dạng single parent, nhưng không muốn sử dụng một HTML element như div