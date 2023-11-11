# Introduction

This document is prepared to specify the sql queries of the "hotel", "reservation", "room", "roomPrice", "season", "
user" tables used in the project.
An image has been added to show the data used in the tables.

# sql query to create a hotel table:

    CREATE TABLE `hotel` (

`hotel_id` int NOT NULL AUTO_INCREMENT,
`hotel_name` varchar(255) COLLATE utf8mb4_general_ci NOT NULL,
`hotel_address` varchar(255) COLLATE utf8mb4_general_ci NOT NULL,
`hotel_city` varchar(255) COLLATE utf8mb4_general_ci NOT NULL,
`hotel_region` varchar(255) COLLATE utf8mb4_general_ci NOT NULL,
`hotel_mail` varchar(255) COLLATE utf8mb4_general_ci NOT NULL,
`hotel_tel` varchar(255) COLLATE utf8mb4_general_ci NOT NULL,
`hotel_star` varchar(255) COLLATE utf8mb4_general_ci NOT NULL,
`hotel_hostel` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_general_ci NOT NULL,
`hotel_feature` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_general_ci NOT NULL,
PRIMARY KEY (`hotel_id`)
) ENGINE=InnoDB AUTO_INCREMENT=52 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci

# simple data insertion for hotel table:

INSERT
INTO `hotel`(`hotel_id`, `hotel_name`, `hotel_address`, `hotel_city`, `hotel_region`, `hotel_mail`, `hotel_tel`, `hotel_star`, `hotel_hostel`, `hotel_feature`)
VALUES
('45','Luxury Hotel','Kızılah Mah. Kolej Sok. 5/A','Ankara','Çankaya','luxury@gmail.com','0312 345 43 44','4 Star','Half
Board, Ultra All Inclusive','Free Parking, Swimming Pool, Hotel Concierge, 7/24 Room Service, SPA, Fitness Center, Free
Wi-fi')

INSERT
INTO `hotel`(`hotel_id`, `hotel_name`, `hotel_address`, `hotel_city`, `hotel_region`, `hotel_mail`, `hotel_tel`, `hotel_star`, `hotel_hostel`, `hotel_feature`)
VALUES
('46','Üsküdar Hotel','Üsküdar mah. İslip sok. 10/A','İstanbul','ÜSküdar','uskudar@gmail.com','0212 234 21 11','5
Star','Ultra All Inclusive, Room Breakfast, Half Board, Full Credit Excluding Alcohol','Free Parking, Fitness Center,
Free Wi-fi, Swimming Pool')

INSERT
INTO `hotel`(`hotel_id`, `hotel_name`, `hotel_address`, `hotel_city`, `hotel_region`, `hotel_mail`, `hotel_tel`, `hotel_star`, `hotel_hostel`, `hotel_feature`)
VALUES
('47','Ankara Hotel','Sinan Cad. Dikmen mah. 4/A','Ankara','Çankaya','ankara@gmail.com','0321 555 11 12','5 Star','All
Inclusive, Ultra All Inclusive','Free Parking, Swimming Pool, Hotel Concierge, 7/24 Room Service, Fitness Center, SPA,
Free Wi-fi')

INSERT
INTO `hotel`(`hotel_id`, `hotel_name`, `hotel_address`, `hotel_city`, `hotel_region`, `hotel_mail`, `hotel_tel`, `hotel_star`, `hotel_hostel`, `hotel_feature`)
VALUES
('49','Acapulco Resort Convention Spa','Girne Çatalköy','Çatalköy','Girne','acapulco@gmil.com','390 243 12 12','5
Star','Ultra All Inclusive, Room Breakfast, All Inclusive, Full Board','Free Wi-fi, Free Parking, Swimming Pool, Hotel
Concierge, 7/24 Room Service, SPA, Fitness Center')

INSERT
INTO `hotel`(`hotel_id`, `hotel_name`, `hotel_address`, `hotel_city`, `hotel_region`, `hotel_mail`, `hotel_tel`, `hotel_star`, `hotel_hostel`, `hotel_feature`)
VALUES
('50','Crytal De Luxe Hotel','Antalya Kemer','Antalya','Kemer','crytal@gmail.com,'390 243 12 12','1 Star','Ultra All
Inclusive, Room Breakfast, All Inclusive, Full Board','Swimming Pool, Fitness Center')

# sql query to create a reservation table:

CREATE TABLE `reservation` (
`reser_id` int NOT NULL AUTO_INCREMENT,
`reser_custom_name` varchar(255) COLLATE utf8mb4_general_ci NOT NULL,
`reser_contact_note` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_general_ci NOT NULL,
`reser_contact_tel` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_general_ci NOT NULL,
`reser_contact_mail` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_general_ci NOT NULL,
`reser_guest_name` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_general_ci NOT NULL,
`reser_guest_nat` varchar(255) COLLATE utf8mb4_general_ci NOT NULL,
`reser_guest_tc` varchar(255) COLLATE utf8mb4_general_ci NOT NULL,
`hotel_id` int NOT NULL,
`reser_checkIn` varchar(255) COLLATE utf8mb4_general_ci NOT NULL,
`reser_checkOut` varchar(255) COLLATE utf8mb4_general_ci NOT NULL,
PRIMARY KEY (`reser_id`)
) ENGINE=InnoDB AUTO_INCREMENT=79 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci

# simple data insertion for hotel table:

INSERT
INTO `reservation`(`reser_id`, `reser_custom_name`, `reser_contact_note`, `reser_contact_tel`, `reser_contact_mail`, `reser_guest_name`, `reser_guest_nat`, `reser_guest_tc`, `hotel_id`, `reser_checkIn`, `reser_checkOut`)
VALUES
('67','Sema Karabulut','rez note.','554 123 43 23','sema@gmail.com','Elif Su Boz','TR','1234321','49','2023-02-02','
2023-02-05')

INSERT
INTO `reservation`(`reser_id`, `reser_custom_name`, `reser_contact_note`, `reser_contact_tel`, `reser_contact_mail`, `reser_guest_name`, `reser_guest_nat`, `reser_guest_tc`, `hotel_id`, `reser_checkIn`, `reser_checkOut`)
VALUES
('68','Sema Karabulut','rez note.','554 123 43 23','sema@gmail.com','Sema Karabulut','TR','453123','49','2023-02-02','
2023-02-05')

INSERT
INTO `reservation`(`reser_id`, `reser_custom_name`, `reser_contact_note`, `reser_contact_tel`, `reser_contact_mail`, `reser_guest_name`, `reser_guest_nat`, `reser_guest_tc`, `hotel_id`, `reser_checkIn`, `reser_checkOut`)
VALUES
('69','ibrahim boz','reser.','542 123 34 45','ibrahim@gmail.com','İbrahim Boz','TR','124512324','45','2023-01-01','
2023-01-02')

INSERT
INTO `reservation`(`reser_id`, `reser_custom_name`, `reser_contact_note`, `reser_contact_tel`, `reser_contact_mail`, `reser_guest_name`, `reser_guest_nat`, `reser_guest_tc`, `hotel_id`, `reser_checkIn`, `reser_checkOut`)
VALUES
('70','busra','res.','423 123 44 12','busra@gmail.com','Busra','TR','5234512','50','2023-01-01','2023-02-02')

INSERT
INTO `reservation`(`reser_id`, `reser_custom_name`, `reser_contact_note`, `reser_contact_tel`, `reser_contact_mail`, `reser_guest_name`, `reser_guest_nat`, `reser_guest_tc`, `hotel_id`, `reser_checkIn`, `reser_checkOut`)
VALUES
('71','busra','res.','423 123 44 12','busra@gmail.com','İbrahim','TR','123453','50','2023-01-01','2023-02-02')

# sql query to create a room table:

CREATE TABLE `room` (
`room_id` int NOT NULL AUTO_INCREMENT,
`hotel_id` int NOT NULL,
`hotel_name` varchar(255) COLLATE utf8mb4_general_ci NOT NULL,
`room_type` varchar(255) COLLATE utf8mb4_general_ci NOT NULL,
`room_bed` int NOT NULL,
`room_stock` int NOT NULL,
`room_tv` tinyint(1) NOT NULL,
`room_minibar` tinyint(1) NOT NULL,
`room_safebox` tinyint(1) NOT NULL,
`room_initial_stock` int NOT NULL,
PRIMARY KEY (`room_id`)
) ENGINE=InnoDB AUTO_INCREMENT=105 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci

# simple data insertion for room table:

INSERT
INTO `room`(`room_id`, `hotel_id`, `hotel_name`, `room_type`, `room_bed`, `room_stock`, `room_tv`, `room_minibar`, `room_safebox`, `room_initial_stock`)
VALUES
('97','45','Luxury Hotel','Suit','2','11','1','0','1','12')

INSERT
INTO `room`(`room_id`, `hotel_id`, `hotel_name`, `room_type`, `room_bed`, `room_stock`, `room_tv`, `room_minibar`, `room_safebox`, `room_initial_stock`)
VALUES
('99','47','Ankara Hotel','Suit','2','3','1','0','1','3')

INSERT
INTO `room`(`room_id`, `hotel_id`, `hotel_name`, `room_type`, `room_bed`, `room_stock`, `room_tv`, `room_minibar`, `room_safebox`, `room_initial_stock`)
VALUES
('101','49','Acapulco Resort Convention Spa','Suit','1','1','1','0','0','2')

INSERT
INTO `room`(`room_id`, `hotel_id`, `hotel_name`, `room_type`, `room_bed`, `room_stock`, `room_tv`, `room_minibar`, `room_safebox`, `room_initial_stock`)
VALUES
('102','50','Crytal De Luxe Hotel','Suit','2','2','1','0','1','3')

INSERT
INTO `room`(`room_id`, `hotel_id`, `hotel_name`, `room_type`, `room_bed`, `room_stock`, `room_tv`, `room_minibar`, `room_safebox`, `room_initial_stock`)
VALUES
('103','51','Fun And Smart Hane Sun','Suit','1','0','1','0','1','2')

# sql query to create a roomPrice table:

CREATE TABLE `roomPrice` (
`roomPrice_id` int NOT NULL AUTO_INCREMENT,
`hostel_type` varchar(255) COLLATE utf8mb4_general_ci NOT NULL,
`hostel_price` int NOT NULL,
`hotel_id` int NOT NULL,
PRIMARY KEY (`roomPrice_id`)
) ENGINE=InnoDB AUTO_INCREMENT=302 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci

# simple data insertion for roomPrice table:

INSERT INTO `roomPrice`(`roomPrice_id`, `hostel_type`, `hostel_price`, `hotel_id`)
VALUES
('257','Half Board','900','45')

INSERT INTO `roomPrice`(`roomPrice_id`, `hostel_type`, `hostel_price`, `hotel_id`)
VALUES
('253','Ultra All Inclusive','800','45')

INSERT INTO `roomPrice`(`roomPrice_id`, `hostel_type`, `hostel_price`, `hotel_id`)
VALUES
('253','All Inclusive','300','45')

INSERT INTO `roomPrice`(`roomPrice_id`, `hostel_type`, `hostel_price`, `hotel_id`)
VALUES
('255','Room Breakfast','120','45')

INSERT INTO `roomPrice`(`roomPrice_id`, `hostel_type`, `hostel_price`, `hotel_id`)
VALUES
('257','Half Board','900','45')

# sql query to create a season table:

CREATE TABLE `season` (
`season_id` int NOT NULL AUTO_INCREMENT,
`hotel_id` int NOT NULL,
`season_name` varchar(255) COLLATE utf8mb4_general_ci NOT NULL,
`start_date` date NOT NULL,
`finish_date` date NOT NULL,
PRIMARY KEY (`season_id`)
) ENGINE=InnoDB AUTO_INCREMENT=47 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci

# simple data insertion for season table:

INSERT INTO `season`(`season_id`, `hotel_id`, `season_name`, `start_date`, `finish_date`)
VALUES
('40','45','Summer Season','2023-01-01','2023-06-06')

INSERT INTO `season`(`season_id`, `hotel_id`, `season_name`, `start_date`, `finish_date`)
VALUES
('42','47','Summer Season','2024-01-01','2024-05-05')

INSERT INTO `season`(`season_id`, `hotel_id`, `season_name`, `start_date`, `finish_date`)
VALUES
('44','50','Summer Season','2023-01-01','2023-03-03')

INSERT INTO `season`(`season_id`, `hotel_id`, `season_name`, `start_date`, `finish_date`)
VALUES
('45','49','Summer Season','2023-02-02','2023-07-07')

INSERT INTO `season`(`season_id`, `hotel_id`, `season_name`, `start_date`, `finish_date`)
VALUES
('46','51','Summer Season','2022-01-01','2023-01-01')

# sql query to create a user table:

CREATE TABLE `user` (
`user_id` int NOT NULL AUTO_INCREMENT,
`user_name` varchar(255) COLLATE utf8mb4_general_ci NOT NULL,
`user_uname` varchar(255) COLLATE utf8mb4_general_ci NOT NULL,
`user_pass` varchar(255) COLLATE utf8mb4_general_ci NOT NULL,
`user_mail` varchar(255) COLLATE utf8mb4_general_ci NOT NULL,
`user_type` enum('admin','user','employee','') COLLATE utf8mb4_general_ci NOT NULL,
PRIMARY KEY (`user_id`)
) ENGINE=InnoDB AUTO_INCREMENT=14 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci

# simple data insertion for user table:

INSERT INTO `user`(`user_id`, `user_name`, `user_uname`, `user_pass`, `user_mail`, `user_type`)
VALUES
('1','ibrahim boz','İbrahim','1','boz@gmail.com','user')

INSERT INTO `user`(`user_id`, `user_name`, `user_uname`, `user_pass`, `user_mail`, `user_type`)
VALUES
('3','Admin','admin','1','admin@gmail.com','admin')

INSERT INTO `user`(`user_id`, `user_name`, `user_uname`, `user_pass`, `user_mail`, `user_type`)
VALUES
('11','Elif Su ','Boz','1','elif@gmail.com','employee')

INSERT INTO `user`(`user_id`, `user_name`, `user_uname`, `user_pass`, `user_mail`, `user_type`)
VALUES
('12','Sema Karabulut ','sema','1','sema@gmail.com','admin')