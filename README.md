# Spotify

Bộ dữ liệu được phân tích thiết kế dựa trên thư viện Spotipy tại nền tảng Spotify - ứng dụng nghe nhạc hang đầu hiện nay. Bộ dữ liệu được lên kế hoạch tự thiết kế và thu thập với trọng tâm là các bài hát tiếng Việt nhằm đánh giá về thị trường âm nhạc Việt Nam. 
	Bộ dữ liệu được thu thập trên nền tảng Google Colab và thư viện có sẵn Spotipy – một thư viện giúp truy xuất dữ liệu dữ liệu được cung cấp từ Spotify một cách dễ dàng và tối ưu. Với thư viện Spotipy, nó cho phép các nhà phát triển có thể truy xuất dữ liệu từ bài hát, nghệ sĩ và album trên số lượng lớn cũng như tìm kiếm và quản lí các nội dung tồn tại trên Spotify.


Bộ dữ liệu thô ban đầu thu thập được bao gồm: 2876 dòng và 23 cột. Sau khi làm sạch và tiền xử lí dữ liệu, nhóm tôi thu được bộ dữ liệu gồm: 2456 dòng 23 cột. Tổng kết, bộ dữ liệu này chứa hơn 2400 bài hát được thu thập từ Spotify với 23 thuộc tính và có tên là “Bộ dữ liệu về các ca khúc tiếng Việt trên nền tảng nghe nhạc trực tuyến Spotify”. Loại dữ liệu của bộ dữ liệu bao gồm các miền dữ liệu về chữ cái, chữ số, kí tự đặc biệt nhưng phổ biến nhất vẫn là chữ cái và số. Qua kiểm tra, có 128 giá trị bị khuyết trong bộ dữ liệu tập trung ở biến album là nhiều nhất do một bài hát có thể thuộc về 1 album hoặc không thuộc album nào nên có thể xuất hiện giá trị null. Nhóm sẽ tiến hành lọc và xóa các bài hát chứa giá trị bị khuyết để đảm bảo độ chính xác và cân bằng của bộ dữ liệu.

Có tổng cộng 23 features trong bộ dữ liệu bao gồm: 
track_uri: dãy định danh của bài hát, nghệ sĩ hoặc album. Dữ liệu là một tập hợp một chuỗi theo định dạng spotify:track[id] với [id] là một chuỗi ký tự gồm 22 chữ cái và số nhằm định danh bài hát. 
track_name: tên bài hát, là tập hợp các kí tự bao gồm chữ cái, số, kí tự đặc biệt đại diện cho tên bài hát. 
artist_name: tên nghệ sĩ, là tập hợp các kí tự bao gồm chữ cái, số, kí tự đặc biệt đại diện cho tên nghệ sĩ sáng tác bài hát.
artist_pop: độ phổ biến của nghệ sĩ sản xuất bài hát. 
artist_genres: thể loại bài hát, là tập hợp các biến mô tả thể loại của bài hát, mỗi bài hát có thể có nhiều thể loại hoặc chưa xác định.
album: tuyển tập ca khúc thuộc về, là tập hợp các kí tự bao gồm chữ cái, số, kí tự đặc biệt mô tả tên của tuyển tập mà bài hát thuộc về. 
track_pop: độ phổ biến của bài hát.
date: thời gian ra mắt, mô tả thời gian ra mắt của ca khúc.
danceability: độ “nhảy” hay độ “bốc” của bài hát.
energy: mức năng lượng, sôi động của bài hát. 
key: khóa hợp âm của bài hát, dựa trên 11 note cơ bản trên khuông nhạc. Mỗi bài hát sẽ có một hợp âm chủ đạo riêng để xác định.
loudness:  âm lượng của bài hát tính bằng dB.
mode: mức độ chỉ âm giai trưởng của bài hát, giá trị gồm 0 và 1 để chị âm giai của bài hát.
speechiness: mức độ lời của bài hát, càng nhiều lời hát thì mức điểm càng cao. Dữ liệu nằm trong khoảng (0-1) và giá trị thực tế nằm trong khoảng [0.0233-0.877]
acousticness: mức độ acoustic của bài hát, được tính trên thang đo (0-1) và giá trị thực tế nằm trong khoảng [0.000053-0.995]
instrumentalness: độ đo xem nhạc bao nhiêu phần trăm là nhạc có lời, bao nhiêu phần trăm là nhạc không lời. Dữ liệu được tính trên thang đo (0-1) và giá trị thực tế nằm trong khoảng [0-0.977]
liveness: mức độ hát live của bài hát được tính trên thang đo (0-1), dữ liệu thực tế có giá trị trong khoảng [0.0245-0.959]
valence: độ tích cực của bài hát.
tempo: nhịp độ của bài hát được tính bằng BPM (beats per minute). 
type: cách phát bài hát tất cả dữ liệu thu được đều là loại audio.
id: định danh của bài hát, là chuỗi kí tự trong track_uri nhằm định danh bài hát
duration_ms: thời lượng bản nhạc.
time_signature: số nhịp của bài hát [1-5].



