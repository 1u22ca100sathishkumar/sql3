# sql3
1. College Table
Create Table
CREATE TABLE College (
    College_Name VARCHAR(100) NOT NULL,
    College_Code INT PRIMARY KEY,
    Course VARCHAR(50) NOT NULL,
    No_of_Students INT CHECK (No_of_Students >= 0)
);

Insert Sample Values
INSERT INTO College (College_Name, College_Code, Course, No_of_Students)
VALUES
('ABC Engineering College', 101, 'Mechatronics', 120),
('XYZ Institute of Technology', 102, 'Computer Science', 150),
('National Engineering College', 103, 'Mechatronics', 95),
('Global Tech University', 104, 'Mechanical', 180),
('Future Engineering College', 105, 'Mechatronics', 140);

Query

Get College Name which has “Mechatronics” course and number of students ≥ 100

SELECT College_Name
FROM College
WHERE Course = 'Mechatronics'
  AND No_of_Students >= 100;

2. Shopping Table
Create Table
CREATE TABLE Shopping (
    Product_ID INT PRIMARY KEY,
    Product_Name VARCHAR(100) NOT NULL,
    Pack_Size VARCHAR(50) NOT NULL,
    Price DECIMAL(10,2) CHECK (Price > 0)
);

Insert Sample Values
INSERT INTO Shopping (Product_ID, Product_Name, Pack_Size, Price)
VALUES
(1, 'Sugar', '500gms', 45.00),
(2, 'Rice', '1kg', 60.00),
(3, 'Tea Powder', '500gms', 120.00),
(4, 'Salt', '250gms', 20.00),
(5, 'Coffee', '500gms', 220.00);

Query

Get details of products which contain 500gms pack

SELECT *
FROM Shopping
WHERE Pack_Size LIKE '%500gms%';
