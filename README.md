

##  Tech Stack

- Python
- Django
- Django REST Framework (DRF)
- MySQL
- JWT Authentication (Djoser)
- Django Signals
- Django Admin Customization
- Media & Image Handling
- Docker (opsional / production-ready)

---

## Database Design (Mandatory Models)

- User (custom user Django)
- UserProfile (OneToOne)
- Category (makanan/minuman)
- Product (menu restoran)
- ProductImage
- Cart
- CartItem
- Order
- OrderItem
- Payment (dummy)
- Review Review

##  PHASE 1 — Setup 

1. Buat Django project `task_django`
2. Buat app: `users`, `menu`, `orders`, `carts`, `reviews`
3. Konfigurasi MySQL sebagai database utama
4. Pastikan migrate berjalan tanpa error
5. Aktifkan Django Debug Toolbar
6. Konfigurasi static files
7. Konfigurasi media files
8. Buat custom Django user model
9. Hubungkan UserProfile (OneToOne)
10. Login admin pakai custom user

---

##  PHASE 2 — Menu & Produk (Core Restaurant)

11. Buat model Category  
12. Buat model Product (nama, harga, deskripsi, stok, is_active)  
13. Relasikan Product ke Category  
14. Tambahkan computed field `is_available`  
15. Sorting menu berdasarkan harga  
16. Filtering menu berdasarkan category  
17. Buat ProductImage model  
18. Hubungkan Product → ProductImage (FK)  
19. Atur upload image ke folder khusus  
20. Pastikan image bisa diakses via API  

---

##  PHASE 3 — Admin Panel (Power User)

21. Register semua model ke admin  
22. Custom `list_display` Product  
23. Admin filter by category  
24. Admin search menu  
25. Inline ProductImage di Product  
26. Custom admin action (nonaktifkan produk)  
27. Tambahkan custom admin link  
28. Validasi harga tidak boleh minus  
29. Edit child object dari parent admin  
30. Buat custom admin form  

---

##  PHASE 4 — ORM Deep Practice

31. Query semua produk aktif  
32. Query produk stok > 0  
33. Gunakan `Q` untuk pencarian kompleks  
34. Gunakan `F` untuk update stok  
35. Gunakan `order_by`  
36. Gunakan `annotate` untuk hitung review  
37. Gunakan `exists()` untuk validasi  
38. `transaction.atomic` saat update stok  
39. Raw SQL query laporan menu  
40. Debug query via Debug Toolbar  

---

##  PHASE 5 — REST API Menu

41. Buat ProductSerializer  
42. Method field (format harga)  
43. CategorySerializer  
44. API list menu  
45. API detail menu  
46. Aktifkan pagination  
47. Aktifkan search  
48. Aktifkan sorting  
49. Produk nonaktif tidak tampil  
50. Uji API via Postman  

---

##  PHASE 6 — Authentication & User System

51. JWT Auth (Djoser)  
52. Endpoint register  
53. Endpoint login  
54. Endpoint refresh token  
55. Endpoint current user  
56. Endpoint protected (login only)  
57. Custom permission admin  
58. Permission di ViewSet  
59. Test akses tanpa token  
60. Inspect JWT payload  

---

##  PHASE 7 — Cart (Keranjang)

61. Model Cart (OneToOne User)  
62. Model CartItem  
63. Add item ke cart  
64. Update jumlah item  
65. Hapus item  
66. Hitung total harga  
67. Validasi stok  
68. Nested serializer  
69. Transaction untuk update cart  
70. Pastikan 1 user = 1 cart  

---

##  PHASE 8 — Checkout & Order

71. Model Order  
72. Model OrderItem  
73. Endpoint checkout  
74. CartItem → OrderItem  
75. Kurangi stok produk  
76. `transaction.atomic`  
77. Return data order  
78. Cegah checkout cart kosong  
79. Update status order  
80. Hanya owner bisa update  

---

##  PHASE 9 — Payment, Signal & Validation

81. Model Payment (dummy)  
82. Payment → Order  
83. Signal saat order dibuat  
84. Auto-create Payment  
85. Update status via signal  
86. Validasi payment  
87. Gunakan `validated_data`  
88. Override `save()` serializer  
89. Cegah double signal  
90. Logging proses order  

---

##  PHASE 10 — Review, Media & Final Polish

91. Model Review  
92. Review → Product & User  
93. 1 user = 1 review  
94. Hitung rating produk  
95. Upload foto review  
96. Validasi file upload  
97. Aktifkan CORS  
98. Frontend bisa akses API  
99. Dokumentasi endpoint  
100. Jelaskan sistem sebagai backend engineer  

---
