## value types & reference types (kiểu tham trị và kiểu tham chiếu)

### 1. Value types (primitive data types)
  - String
  - Number
  - Boolean
  - BigInt
  - Symbol
  - undefine
  - null

  * kiểu dữ liệu nguyên thủy : khi gán 1 giá trị thì nó sẽ lưu giá trị đó
  * tại một thời điểm chỉ lưu 1 giá trị

  * cách thức hoạt động
    - khi tạo 1 biến let a = 1, tạo ô nhớ , cấp vào một ô nhớ , lưu 1 vào ô nhớ
    - let b = a: Tạo ra biến b, cấp một ô nhớ khác, sao chép giá trị của a vào ô nhớ mới
    - a = 2 , sửa giá trị trong ô nhớ a = 2 

### 2. Reference types
  - Object
  - Array
  - Function

  * cách thức hoạt động
    - khi tạo 1 biến let a = { name : 'a' }, tạo ô nhớ , cấp vào một ô nhớ , lưu { name : 'a' } vào ô nhớ, trả về địa chỉ đã lưu và gán cho biến a
    - let b = a: Tạo ra biến b, trỏ biến b đến địa chỉ ô nhớ của biến a
    - a.name = 'b' , sửa giá trị key name trong ô nhớ thành 'b' 

## Data types with function
  * ex: function func(obj) {
          // thực chất là đang khai báo: obj.name = 'mec'
          obj.name = 'bmv'
          console.log(obj)
        }

        const a = { name: 'mec' }
        func(a)
        console.log(a)

        // side effect: tác dụng phụ , điều xảy ra ko mong muốn

  * các cách khác phục 
    + spred operator , Object.asign (ko giải quyết đc vấn đề nested Object)
    + JSON.parse(JSON.stringify(originalObject)) (giải quyết đc nested Object tuy nhiên vs dữ liệu lớn ảnh hưởng đến perfomance)
    + dùng thư viện :))