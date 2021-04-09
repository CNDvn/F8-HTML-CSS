# Front-End
## Vài tag phổ biến
1. h1 - h6 :heading
2. p :paragraph
3. img :image
4. a :achor
5. ul, li :unordered list, list item
6. table
7. input
8. button
9. div

## Đơn vị
1. Absolute units (Đơn vị tuyệt đối): kích thước cố định, không thay đổi khi các yếu tố xung quanh tác động vào, như thu nhỏ/phóng to trình duyệt
- px
- pt
- cm
- mm
- inch
- pc
2. Relative units (Đơn vị tương đối: phải có đứa để phụ thuộc vào): kích thước không cố định, bị thay đổi khi đối tượng mà nó phụ thuộc vào bị thay đổi
- %: phụ thuộc vào thẻ chứa nó (mặc định 100% = 16px)
- rem: phụ thuộc vào thẻ html
- em: phụ thuộc vào thẻ gần nhất chứa nó (mặc định 1em = 16px)
- vw(viewport width): phụ thuộc vào chiều ngang của trình duyệt (ex: 50vw = 50%vw)
- vh(viewport height): phụ thuộc vào chiều dọc của trình duyệt (ex: 50vh = 50%vh)
- vmin
- vmax
- ex
- ch

## độ ưu tiên
1. Internal, External (thằng nào ở sau thì gọi apply thằng đó)
2. Inline - 1000
3. #id - 100
4. .class - 10
5. tag - 1
6. Equal specificity?
7. Universal selector and inherited

## Position (có thêm top left righ bottom khi dùng thuộc tính này)
1.Relative: tương đối
    + không bị phụ thuộc vào đối tượng nào khác cả, lấy chính vị trí đang đứng để làm gốc tọa độ => phụ thuộc vào chính nó
2.Absolute: tuyệt đối
    + phụ thuộc thẻ cha gần nhất có thuộc tính position để lấy cha đó làm gốc tọa độ
3.Fixed: phụ thuộc vào khung trình duyệt
    + vị trí phụ thuộc vào khung của trình duyệt
4.Sticky: bám dính phụ thuộc vào khung trình duyệt

## Breakpoints: là những điểm/vị trí mà bố cục website sẽ thay đổi - thích ứng để tạo nên giao diện responsive
- Mobile: width < 740px
- Tablet: width >= 740px and width < 1024px
- PC: width >= 1024px

## Flexbox
- display: flex|inline-flex - quyết định có sử dụng flex hay không
- flex-direction: row|column - thay đổi phương hướng của main axis
- flex-wrap: nowrap|wrap (xuống dòng) |wrap-reverse (nhẩy lên trên | đảo chiều cross start và cross end) - ...
- flex-basic:<lenght> - set kích thước cho main size
- justify-content: flex-start|flex-end|center|space-between(cách các flex item)|space-around(cách các flex item)|space-evenly - căn được những flex item theo phương main axis (dành cho cha nếu set cho cha thì con không cần dùng justify-self vì khi dùng thằng này ở cha thì ở con nó đã tự set justify-self rồi)
- justify-self: flex-start|flex-end|center
- align-content: flex-start|flex-end|center - giống justify-content nhưng theo phương cross axis
- align-self:flex-start|flex-end|center - tương tự justify-self
- flex-grow: <number> - thay đổi kích thước main size
- flex-shrink: <number> - ngược lại flex-grow (thu nhỏ lại)
- flex: <flex-grow>|<flex-shrink>|<flex-basic> - shorthand của flex-basic + flex-grow + flex-shrink
- flex-flow:<number>  - shorthand của flex-wrap + flex-direction
- order: <number> - quyết định thứ tự flex item được hiển thị xem thằng nào trước thằng nào sau
* tham khảo:
    https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Flexbox#the_flex_model
* Ôn luyện bằng: https://codepen.io/enxaneta/full/adLPwv/

## BEM
- là tiêu chuẩn đặt tên class khi viết CSS
### Ý nghĩa
- Viết tắt của: BLock Element Modifier
- Block: khối
- Element: thành phần của khối
- Modifier: Bổ sung ý nghĩa cho `Block` hoặc `Element`
### Tại sao dùng BEM
- Mỗi người đặt một kiểu
- Members đặt class trùng nhau, CSS đè lên nhau
### Cú pháp
