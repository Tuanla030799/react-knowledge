### tại sao cần keys cho react list ?
  - keys là một giá trị duy nhất bạn có thể truyền nó cho key prop khi dùng .map() function để xử lý các element hoặc component trong list
  - bạn cần dùng keys cho react lists bởi vì keys giuwsp react nhận biết và phân biệt đc các component
  - nếu không thì khi bạn thay đổi các items trong list bằng cách thêm mới hoặc chỉnh sửa chúng, thì react sẽ không biết thứ tự sắp xếp chúng. Đó là bởi vì React sẽ xử lí các việc cập nhật DOM cho chúng ta nhưng react cần dùng đến keys để cập nhạt chúng một cách chính xác
  - Khi state trong component thay đổi, hàm render() sẽ trả về một tree mới (a new tree of React elements), khác với tree cũ lúc state chưa thay đổi. ReactJS sẽ tìm ra những điểm khác biệt thông qua thuật toán diffing và update lại chúng trên UI. Quá trình match tree cũ và tree mới gọi là reconciliation
  - không nên sử dụng key là index bởi vì nếu key là index thì khi ta thay đổi vị trí của các phần tử trong mảng (xóa, thêm...), index cũng sẽ thay đổi và lại xảy ra vấn đề

### ref là gì và thường được sử dụng ntn ?
  - 𝐑𝐞𝐟 là một tham chiếu của DOM element trong React. Ref được tạo với sự trợ giúp của Useref Hook và có thể được đặt ngay lập tức trong một biến. Biến này sau đó được chuyển đến một React element (không phải là một component) để có được tham chiếu đến DOM element bên dưới (nghĩa là div, span, v.v.). Bản thân element và các thuộc tính của nó có thể được sử dụng bằng cách gọi .current của ref đó.

 - Ref thường được biết đến như là “Escape hatch” để có thể làm việc với DOM element trực tiếp. Chúng cho phép bạn thực hiện một vài hành động nhất định mà không thể thực hiện thông qua React nếu không có Ref như là clear hoặc focus một input.

### ueseeffect được sử dụng để làm gì
  - useEffect hook được sử dụng để thực hiện các side efect trong các React components
  - Side effect là các phép toán được thực hiện với “thế giới bên ngoài” hoặc là một số thứ nằm bên ngoài context của React app
  - Một vài ví dụ của side effect có thể kể đến là thực hiện một GET hoặc POST request đến external API hoặc làm việc với một browser API như là 𝐰𝐢𝐧𝐝𝐨𝐰.𝐧𝐚𝐯𝐢𝐠𝐚𝐭𝐨𝐫 hoặc là 𝐝𝐨𝐜𝐮𝐦𝐞𝐧𝐭.𝐠𝐞𝐭𝐄𝐥𝐞𝐦𝐞𝐧𝐭𝐁𝐲𝐈𝐝().
  - Bạn không thể thực hiện các câu lệnh này trực tiếp trong body của React component. useEffect là một function giúp bạn có thể thực hiện các side effects, và bạn có thể sẽ cần khai báo một mảng dependencies chứa các giá trị bên ngoài mà function đó cần để hoạt động.
  - Nếu có bất kỳ giá trị nào trong mảng dependencies thay đổi thì function effect sẽ được chạy lại.

### useCallback và useMemo dùng để làm gì ?
  - useCallback vs useMeme được sử dụng để cải thiện component performance.
  - useCallback được sử dụng để ngăn ngừa các functions được khai báo bên trong components khỏi việc liên tục bị tạo lại trong mỗi lần render. Điều này có thể dẫn giảm hiệu năng đặc biệt là callback function được truyền tới component con.props drilling” - là khi mà bạn truyền data bằng props qua các components không cần sử dụng đến chúng.
  - Mặc khác, useMemo sẽ ghi nhớ các phép toán phức tạp. Hiểu một cách đơn giản, bạn có thể có một phép toán mà chiếm một khối lượng tài nguyên cần thiết để tính toán và bạn muốn nó được thực hiện một cách hiệu quả nhất. Trong trường hợp đó, bạn sẽ muốn sử dụng useMemo hook thay vì useCallback hook vì nó trả về một giá trị chứ không phải một function