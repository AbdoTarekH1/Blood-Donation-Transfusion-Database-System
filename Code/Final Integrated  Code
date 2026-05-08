CREATE SCHEMA Blood_Donation_and_Transfusion_Database;
USE Blood_Donation_and_Transfusion_Database;

-- Created Donor table that holds Donors' information
CREATE TABLE Donor(
DonorID INT PRIMARY KEY NOT NULL,
FirstName VARCHAR(30) NOT NULL,
LastName VARCHAR(30) NOT NULL,
Gender ENUM('Male','Female') NOT NULL,
BloodType ENUM('A+' , 'A-', 'B+','B-', 'AB+','AB-','O+','O-') NOT NULL ,
LastDonationDate DATE NOT NULL,
DateOfBirth DATE NOT NULL
);

-- Created Donor_Phone table that holds Donors' Phone numbers
CREATE TABLE Donor_Phone(
DonorID INT NOT NULL,
Phone_Number VARCHAR(15) NOT NULL,

-- This table's primary keys are a combination between DonorID and the Phone_Number 
PRIMARY KEY (DonorID, Phone_Number),

-- DonorID is a foreign key from the Donor table that helps us know which Donor we are dealing with
CONSTRAINT FK_Donor_Phone FOREIGN KEY (DonorID) REFERENCES Donor(DonorID) ON DELETE CASCADE
);

-- Insert Donors' information to the Donor table
INSERT INTO Donor VALUES 
(001, 'Abdelrahman', 'Haggag', 'Male', 'AB+', '2024-12-06', '2006-03-24'),
(002, 'Ahmed', 'Mazhar', 'Male', 'A+', '2024-06-02', '2004-07-29'),
(003, 'Ahmed', 'Jabr', 'Male', 'B-', '2023-04-25', '2005-10-06'), 
(004, 'Ibrahim', 'Ammar', 'Male', 'A-', '2024-11-11', '1997-12-20'),
(005, 'Jana', 'Ismail', 'Female', 'A-', '2024-06-24', '1991-12-14'),
(006, 'Logy', 'Khalil', 'Female', 'AB-', '2024-12-03', '1984-04-08'),
(007, 'Mariam', 'Bakr', 'Female', 'B-', '2024-11-30', '1982-05-27'),
(008, 'Fatma', 'Tawfik', 'Female', 'O-', '2023-07-07', '1996-05-21'),
(009, 'Ahmed', 'Badawi', 'Male', 'AB-', '2024-05-15', '1999-09-10'),
(010, 'Suzan', 'Soliman', 'Female', 'B-', '2024-01-06', '2005-01-01'),
(011, 'Wael', 'Farahat', 'Male', 'O+', '2024-12-28', '1985-05-22'),
(012, 'Jana', 'Ghanem', 'Female', 'O-', '2023-07-23', '1984-03-03'),
(013, 'Samy', 'Amin', 'Male', 'O-', '2023-01-09', '2001-05-20'),
(014, 'Samy', 'Shaheen', 'Male', 'B-', '2023-12-18', '1998-10-17'),
(015, 'Malak', 'Zaki', 'Female', 'O+', '2024-12-11', '1999-04-10'),
(016, 'Yassin', 'Gaber', 'Male', 'AB+', '2023-07-19', '1996-01-08'),
(017, 'Shahd', 'Kamal', 'Female', 'A-', '2024-06-06', '1997-03-19'),
(018, 'Rawan', 'Hassan', 'Female', 'B-', '2023-11-05', '1987-06-02'),
(019, 'Nour', 'Mansour', 'Female', 'A-', '2024-07-13', '2005-02-16'),
(020, 'Hady', 'Fawzy', 'Male', 'AB+', '2023-02-16', '1983-11-15'),
(021, 'Salma', 'Badawi', 'Female', 'B-', '2023-01-27', '1995-02-10'),
(022, 'Tarek', 'Youssef', 'Male', 'A-', '2023-08-28', '1985-10-04'),
(023, 'Judy', 'Riad', 'Female', 'B+', '2023-03-20', '1989-05-02'),
(024, 'Nour', 'Salem', 'Female', 'B+', '2023-06-27', '1992-04-01'), 
(025, 'Tarek', 'Farahat', 'Male', 'AB+', '2023-05-10', '1981-09-24'),
(026, 'Samy', 'Hany', 'Male', 'B+', '2023-01-27', '1995-04-23'),
(027, 'Yassin', 'Mounir', 'Male', 'A+', '2024-10-18', '1987-06-01'),
(028, 'Shahd', 'Riad', 'Female', 'B-', '2023-11-19', '1997-09-11');

SET FOREIGN_KEY_CHECKS = 0;
TRUNCATE TABLE Donor;
SET FOREIGN_KEY_CHECKS = 1;

-- Insert Donors' Phone numbers to the Donor_Phone table
INSERT INTO Donor_Phone VALUES
(001, '+201208864464'),
(002, '+201105487648'), -- Patient 002 has 2 phone number
(002, '+201058774685'),
(003, '+201500587746'),
(003, '+966556573075'),
(004, '+201012345678'),
(005, '+201112345679'),
(005, '+201212345680'),
(006, '+201512345681'),
(007, '+201022334455'),
(008, '+201122334456'),
(009, '+201222334457'),
(010, '+201522334458'), -- Patient 010 has 2 phone number
(010, '+966501234567'),
(011, '+201033445566'),
(012, '+201133445567'),
(013, '+201233445568'),
(014, '+201533445569'),
(015, '+201044556677'),
(016, '+201144556678'),
(017, '+201244556679'),
(018, '+201544556680'),
(019, '+201055667788'),
(020, '+201155667789'),
(021, '+201255667790'),
(022, '+201555667791'),
(023, '+201066778892'),
(024, '+201166778893'),
(025, '+201266778894'),
(025, '+966559876543'),
(026, '+201566778895'),
(027, '+201077889906'),
(028, '+201177889907');

SET FOREIGN_KEY_CHECKS = 0;
TRUNCATE TABLE Donor_Phone;
SET FOREIGN_KEY_CHECKS = 1;

-- View all the information in the Donor table
SELECT * FROM Donor;

-- View all the information in the Donor_Phone table
SELECT * FROM Donor_Phone;

-- Create the BloodBank table
CREATE TABLE BloodBank (
BankID INT NOT NULL,
BankName Varchar(30) NOT NULL,
Address varchar(40) NOT NULL,
City Varchar(40) NOT NULL,
TotalCapacityUnits INT NOT NULL,

PRIMARY KEY (BankID)

);

INSERT INTO BloodBank (BankID, BankName, Address, City, TotalCapacityUnits) VALUES
(001, 'National Blood Transfusion Ctr', '51 Ministry of Agriculture St', 'Giza', 5000),
(002, 'Kasr Al-Ainy Blood Bank', 'Kasr Al-Ainy Hospital, Al Saraya St', 'Cairo', 3500),
(003, 'Abbassia Blood Transfusion', 'Next to Abbassia Fever Hospital', 'Cairo', 3000),
(004, 'Demerdash Hospital Bank', 'Ramses Street, Ain Shams University', 'Cairo', 2500),
(005, 'Egyptian Red Crescent Bank', 'Youssef Abbas Street', 'Cairo', 2000),
(006, 'Regional Blood Transfusion Ctr', 'Kom Al Dikka Square', 'Alexandria', 4000),
(007, 'Al Miri Hospital Blood Bank', 'College of Medicine Street', 'Alexandria', 2800),
(008, 'Tanta Regional Blood Center', 'Al Baher St, Next to Governorate HQ', 'Gharbia', 2200),
(009, 'Mansoura University Bank', 'Al Mashaya Al Sifliya Street', 'Dakahlia', 3200),
(010, 'Assiut Regional Blood Center', 'Corniche Al Nil Street', 'Assiut', 2500),
(011, 'Sohag University Hospital Bank', 'Nasr City, East of the Nile', 'Sohag', 1800),
(012, 'Zagazig Transfusion Center', 'Sharkia Governorate Street', 'Sharkia', 2100),
(013, 'Beni Suef University Bank', 'East of the Nile, University Complex', 'Beni Suef', 1500),
(014, 'Ismailia Regional Center', 'Sheikh Zayed District', 'Ismailia', 2000),
(015, 'Minia General Hospital Bank', 'Al Horreya Street', 'Minia', 1700),
(016, 'Benha University Blood Bank', 'Fareed Nadda Street', 'Qalyubia', 1900),
(017, 'Port Said Transfusion Center', 'Kisra and Al Geish Street', 'Port Said', 1600),
(018, 'Shebin El Kom Blood Bank', 'Gamal Abdel Nasser Street', 'Menofia', 2000),
(019, 'Luxor Regional Blood Center', 'Television Street', 'Luxor', 1400),
(020, 'Aswan University Hospital Bank', 'Al Sadat Road', 'Aswan', 1500);

SELECT * FROM BloodBank;

-- Create the Bank_Phone table for the multivalued attribute (Bank_Phone).
CREATE TABLE Bank_Phone (
BankID INT NOT NULL,
PhoneNumber VARCHAR(15) NOT NULL,
    
-- The Primary Key is a combination of both to allow one hospital to have multiple numbers
PRIMARY KEY (BankID, PhoneNumber),
    
-- Foreign Key to link back to the Hospital
CONSTRAINT FK_Bank_Phone FOREIGN KEY (BankID) 
	REFERENCES BloodBank(BankID) ON DELETE CASCADE
);

INSERT INTO Bank_Phone (BankID, PhoneNumber) VALUES
(001, '0223912143'), -- National Blood Transfusion Ctr
(002, '01001234567'),
(003, '0223646361'), -- Kasr Al-Ainy
(004, '0223654060'),
(005, '0226844360'), -- Abbassia
(006, '0224821911'), -- Demerdash
(006, '0226703106'), -- Red Crescent
(007, '034847361'),  -- Alexandria Regional
(008, '034847362'),
(009, '034862244'),  -- Al Miri Hospital
(010, '0403334053'), -- Tanta
(011, '0502202022'), -- Mansoura University
(012, '0882332208'), -- Assiut
(013, '0934601744'), -- Sohag
(014, '0552304866'), -- Zagazig
(015, '0822245020'), -- Beni Suef
(016, '0643206944'), -- Ismailia
(017, '0862342500'), -- Minia
(018, '0133222361'), -- Benha
(019, '0663222920'), -- Port Said
(020, '0482222711'); -- Shebin El Kom 

SELECT * FROM Bank_Phone;

-- Create the Hospital table 
CREATE TABLE Hospital(
HospitalID INT NOT NULL,
HospitalName VARCHAR(150) NOT NULL,
Address VARCHAR(255) NOT NULL,
City VARCHAR(100) NOT NULL,

-- Assign HospitalID as Primary Key.

PRIMARY KEY (HospitalID)

);

-- Insert Hospitals' information to the Hospital table
INSERT INTO Hospital VALUES 
(001, 'Al Salam International Hospital', 'Corniche El Nil, Maadi', 'Cairo'),
(002, 'Dar Al Fouad Hospital', '26th of July Corridor, 6th of October City', 'Giza'),
(003, 'Andalusia Hospital Smouha', 'Smouha, Victor Emanuel Square', 'Alexandria'),
(004, 'As-Salam International Hospital', 'Corniche El Nil', 'Cairo'),
(005, 'Cleopatra Hospital', '39 Cleopatra Street, Heliopolis', 'Cairo'),
(006, 'Saudi German Hospital', 'Joseph Tito St, El Nozha', 'Cairo'),
(007, 'Magdi Yacoub Heart Foundation', 'Aswan Square', 'Aswan'),
(008, 'El Gezira Hospital', '12 Mohamed Anis St, Zamalek', 'Cairo'),
(009, 'International Medical Center', 'Cairo-Ismailia Desert Road', 'Cairo'),
(10, 'Children’s Cancer Hospital Egypt 57357', '1 Seket Al-Imam, El-Sayeda Zeinab', 'Cairo'),
(011, 'Mowasat Hospital', 'Horreya Road, Hadara', 'Alexandria'),
(012, 'Mansoura University Hospital', 'Gomhouria St', 'Mansoura'),
(013, 'Suez Canal University Hospital', 'Ring Road', 'Ismailia'),
(014, 'Nile Badrawi Hospital', 'Corniche El Maadi', 'Cairo'),
(015, 'Air Force Specialized Hospital', '90th North St, Fifth Settlement', 'Cairo'),
(016, 'Wadi El Neel Hospital', 'Hadayek El Kobba', 'Cairo'),
(017, 'Prime Health Medical Center', 'New Cairo', 'Cairo'),
(018, 'Alexandria Medical Center', '14 May Bridge Road, Smouha', 'Alexandria'),
(019, 'Borg Al Arab University Hospital', 'New Borg El Arab', 'Alexandria'),
(020, 'Tanta University Hospital', 'El-Geish Street', 'Tanta');

-- View all the information in the Donor table
SELECT * FROM Hospital;

-- Create the Hospital_Phone table for the multivalued attribute (Hospital_Phone).
CREATE TABLE Hospital_Phone (
HospitalID INT NOT NULL,
PhoneNumber VARCHAR(15) NOT NULL,
    
-- The Primary Key is a combination of both to allow one hospital to have multiple numbers
PRIMARY KEY (HospitalID, PhoneNumber),
    
-- Foreign Key to link back to the Hospital
CONSTRAINT FK_Hospital_Phone FOREIGN KEY (HospitalID) 
	REFERENCES Hospital(HospitalID) ON DELETE CASCADE
);

-- Insert Hospital_Phone_Numbers' information to the Hospital_Phone table
INSERT INTO Hospital_Phone VALUES 
(001, '02-25550101'),
(001, '19101'),
(002, '02-35550202'),
(003, '03-45550303'),
(004, '010-12345678'),
(005, '011-23456789'),
(006, '012-34567890'),
(007, '015-45678901'),
(007, '02-27778888'),
(008, '03-58880808'),
(009, '050-2345090'),
(010, '040-3344110'),
(011, '088-2111222'),
(012, '097-3111333'),
(013, '064-3222444'),
(014, '062-3333555'),
(015, '066-3444666'),
(016, '010-98765432'),
(017, '012-87654321'),
(018, '16118'),
(019, '02-29991111'),
(020, '011-55554444');

-- View all the information in the Donor table
SELECT * FROM Hospital_Phone;

-- Create the BloodUnit table with updated constraints.
CREATE TABLE BloodUnit(
UnitID INT NOT NULL,
BankID INT NOT NULL,
DonorID INT NOT NULL,
CollectionDate DATE,
ExpiryDate Date,
Status_of_Unit ENUM('Available', 'Expired', 'Reserved', 'Transfused') DEFAULT 'Available',

-- Assign UnitID, BankID as Primary Key.
PRIMARY KEY (UnitID , BankID),

-- We have BankID , DonorID as Foreign Key.
CONSTRAINT FK_Bank_Unit FOREIGN KEY (BankID) 
	REFERENCES BloodBank(BankID) ON DELETE CASCADE,
CONSTRAINT FK_Donor_Unit FOREIGN KEY (DonorID) 
	REFERENCES Donor(DonorID) ON DELETE CASCADE,

-- Ensure that the Expire is after the Collection.  

CONSTRAINT chk_dates CHECK (ExpiryDate > CollectionDate)

);

-- Derived Attribute: Automatic Expiry Tracking (Calculated at Runtime)
CREATE OR REPLACE VIEW View_BloodUnit_Status AS
SELECT 
    UnitID, 
    BankID,
    ExpiryDate,
    Status_of_Unit AS OriginalStatus,
    -- If it's physically expired, the status is 'Expired' regardless of the table column
    -- Otherwise, it shows whatever is in the table (Available, Reserved, etc.)
    CASE 
        WHEN ExpiryDate < CURDATE() THEN 'Expired'
        ELSE Status_of_Unit
    END AS FinalStatus
FROM BloodUnit;

-- Insert BloodUnits' information to the BloodUnit table
INSERT INTO BloodUnit  VALUES
(001, 001, 001, '2026-04-15', '2026-05-27', 'Available'),
(002, 001, 002, '2026-04-16', '2026-05-28', 'Available'),
(003, 002, 003, '2026-03-20', '2026-05-01', 'Expired'),
(004, 002, 004, '2026-04-20', '2026-06-01', 'Available'),
(005, 003, 005, '2026-04-25', '2026-06-06', 'Reserved'),
(006, 003, 006, '2026-04-26', '2026-06-07', 'Available'),
(007, 004, 007, '2025-12-01', '2026-01-12', 'Transfused'),
(008, 004, 008, '2026-05-01', '2026-06-12', 'Available'),
(009, 005, 009, '2026-05-02', '2026-06-13', 'Available'),
(010, 005, 010, '2026-03-10', '2026-04-21', 'Expired'),
(011, 001, 011, '2026-04-28', '2026-06-09', 'Available'),
(012, 001, 012, '2026-04-29', '2026-06-10', 'Available'),
(013, 002, 013, '2026-04-30', '2026-06-11', 'Reserved'),
(014, 002, 014, '2026-05-03', '2026-06-14', 'Available'),
(015, 003, 015, '2026-01-15', '2026-02-26', 'Transfused'),
(016, 003, 016, '2026-05-04', '2026-06-15', 'Available'),
(017, 004, 017, '2026-05-05', '2026-06-16', 'Available'),
(018, 004, 018, '2026-05-06', '2026-06-17', 'Available'),
(019, 005, 019, '2026-02-10', '2026-03-24', 'Expired'),
(020, 005, 020, '2026-05-07', '2026-06-18', 'Available');

-- View all the information in the BloodUnit table
SELECT * FROM BloodUnit;

-- Create the BloodInventory table with updated constraints.
CREATE TABLE BloodInventory (
BankID INT NOT NULL,
BloodType ENUM('A+' , 'A-', 'B+','B-', 'AB+','AB-','O+','O-') NOT NULL , 
Quantatity_Available INT DEFAULT 0,
LastUpdate Date,

PRIMARY KEY(BankID, BloodType),

CONSTRAINT FK_BloodBank_Inventory FOREIGN KEY (BankID) REFERENCES BloodBank(BankID) ON DELETE CASCADE
);

DELIMITER //
CREATE TRIGGER After_BloodUnit_Insert
AFTER INSERT ON BloodUnit
FOR EACH ROW
BEGIN
    UPDATE BloodInventory 
    SET Quantatity_Available = Quantatity_Available + 1,
        LastUpdate = CURDATE()
    WHERE BankID = NEW.BankID 
      AND BloodType = (SELECT BloodType FROM Donor WHERE DonorID = NEW.DonorID);
END //
DELIMITER ; 

DELIMITER //
CREATE TRIGGER After_BloodUnit_Delete
AFTER DELETE ON BloodUnit
FOR EACH ROW
BEGIN
    UPDATE BloodInventory 
    SET Quantatity_Available = Quantatity_Available - 1,
        LastUpdate = CURDATE()
    WHERE BankID = OLD.BankID 
      AND BloodType = (SELECT BloodType FROM Donor WHERE DonorID = OLD.DonorID);
END //
DELIMITER ;

INSERT INTO BloodInventory (BankID, BloodType, Quantatity_Available, LastUpdate) VALUES
(001, 'A+', 50, '2026-05-01'),
(002, 'O-', 12, '2026-05-02'),
(003, 'B+', 35, '2026-05-01'),
(004, 'AB+', 10, '2026-05-03'),
(005, 'A-', 20, '2026-05-01'),
(006, 'O+', 100, '2026-04-28'),
(007, 'B-', 8, '2026-05-01'),
(008, 'AB-', 5, '2026-05-02'),
(009, 'A+', 45, '2026-05-01'),
(010, 'O-', 15, '2026-05-04'),
(011, 'B+', 25, '2026-05-01'),
(012, 'O+', 80, '2026-05-03'),
(013, 'AB+', 12, '2026-05-01'),
(014, 'A-', 18, '2026-05-02'),
(015, 'B-', 7, '2026-05-01'),
(016, 'O-', 20, '2026-05-05'),
(017, 'AB-', 4, '2026-05-01'),
(018, 'A+', 60, '2026-05-02'),
(019, 'B+', 30, '2026-05-01'),
(020, 'O+', 90, '2026-05-04');

SELECT * FROM BloodInventory;

-- Created Patient table that holds Patients' information
CREATE TABLE Patient(
PatientID INT NOT NULL,
HospitalID INT NOT NULL,
FirstName VARCHAR(30) NOT NULL,
LastName VARCHAR(30) NOT NULL,
Gender ENUM('Male','Female') NOT NULL,
BloodType ENUM('A+' , 'A-', 'B+','B-', 'AB+','AB-','O+','O-') NOT NULL ,
DateOfBirth DATE NOT NULL,

-- This table's primary keys are a combination between PatientID and the HospitalID
PRIMARY KEY(PatientID, HospitalID),

-- HospitalID is a foreign key from the Hospital table that tells us which Hospital we are dealing with
CONSTRAINT FK_Hospital_Patient FOREIGN KEY (HospitalID) REFERENCES Hospital(HospitalID) ON DELETE CASCADE
);

-- Created Patient_Phone table that holds Patients' Phone numbers
CREATE TABLE Patient_Phone(
PatientID INT NOT NULL,
HospitalID INT NOT NULL,
Phone_Number VARCHAR(15) NOT NULL,

-- This table's primary keys are a combination between DonorID and the Phone_Number
PRIMARY KEY (PatientID, Phone_Number),

-- PatientID is a foreign key from the Patient table that helps us know which Patient we are dealing with
CONSTRAINT FK_Patient_Phone FOREIGN KEY (PatientID, HospitalID) REFERENCES Patient(PatientID, HospitalID) ON DELETE CASCADE
);

-- Insert Patients' information to the table
INSERT INTO Patient VALUES
(001, 001, 'Mohamed', 'Salama', 'Male', 'AB-', '2006-08-09'),
(002, 002, 'Abdelrahman', 'Nawar', 'Male', 'B-', '2005-06-29'),
(003, 003, 'Ziad', 'Zaza', 'Male', 'O+', '2000-05-14'),
(004, 004, 'Omar', 'Khattab', 'Male', 'A+', '1995-03-12'),
(005, 005, 'Laila', 'Hassan', 'Female', 'O-', '1988-11-20'),
(006, 006, 'Youssef', 'Aly', 'Male', 'AB+', '2002-01-15'),
(007, 007, 'Sara', 'Ibrahim', 'Female', 'B+', '1999-07-30'),
(008, 008, 'Mostafa', 'Kamal', 'Male', 'A-', '1991-04-05'),
(009, 009, 'Mariam', 'Zaki', 'Female', 'O+', '2004-09-18'),
(010, 010, 'Hamza', 'Farid', 'Male', 'B-', '1985-12-25'),
(011, 011, 'Nour', 'Eldin', 'Female', 'AB-', '2000-06-10'),
(012, 012, 'Khaled', 'Saad', 'Male', 'A+', '1993-02-28'),
(013, 013, 'Fatma', 'Rashed', 'Female', 'O-', '1982-10-05'),
(014, 014, 'Tarek', 'Mahmoud', 'Male', 'B+', '1997-08-14'),
(015, 015, 'Hana', 'Samy', 'Female', 'AB+', '2003-05-22'),
(016, 016, 'Ziad', 'Salem', 'Male', 'A-', '1990-11-11'),
(017, 017, 'Aya', 'Gaber', 'Female', 'O+', '1996-03-03'),
(018, 018, 'Ibrahim', 'Nasr', 'Male', 'B-', '1989-12-12'),
(019, 019, 'Salma', 'Fawzy', 'Female', 'AB-', '2005-01-01'),
(020, 020, 'Marwan', 'Badawi', 'Male', 'A+', '1994-07-07'),
(021, 001, 'Habiba', 'Amr', 'Female', 'O-', '2001-04-20'),
(022, 002, 'Karim', 'Abbas', 'Male', 'B+', '1987-09-15'),
(023, 003, 'Jana', 'Khalil', 'Female', 'AB+', '1998-02-10'),
(024, 004, 'Sherif', 'Mounir', 'Male', 'A-', '1992-06-24'),
(025, 005, 'Farida', 'Osman', 'Female', 'O+', '2000-10-30'),
(026, 006, 'Adel', 'Emam', 'Male', 'B-', '1984-05-17'),
(027, 007, 'Dina', 'Elsherbiny', 'Female', 'AB-', '1996-08-08'),
(028, 008, 'Yassin', 'Tohamy', 'Male', 'A+', '2002-12-12');

DROP TABLE Patient;
DROP TABLE Patient_Phone;
SET FOREIGN_KEY_CHECKS = 0;
TRUNCATE TABLE Patient;
SET FOREIGN_KEY_CHECKS = 1;

-- Insert Patients' Phone numbers to the Patient_Phone table
INSERT INTO Patient_Phone (PatientID, HospitalID, Phone_Number) VALUES
(001, 001, '+201055482144'),
(002, 002, '+201258792604'),
(002, 002, '+201002530648'), -- Patient 002 has two phone numbers
(003, 003, '+201154684884'), 
(004, 004, '+201011112222'), 
(005, 005, '+201111112223'), 
(006, 006, '+201211112224'), 
(007, 007, '+201511112225'), 
(008, 008, '+201022223333'), 
(008, 008, '+201122223334'), -- Patient 008 has two phone numbers
(009, 009, '+201222223335'), 
(010, 010, '+201522223336'), 
(011, 011, '+201033334444'), 
(012, 012, '+201133334445'), 
(013, 013, '+201233334446'), 
(014, 014, '+201533334447'), 
(015, 015, '+201044445555'), 
(016, 016, '+201144445556'), 
(017, 017, '+201244445557'), 
(018, 018, '+201544445558'), 
(019, 019, '+201055556666'), 
(020, 020, '+201155556667'), 
(021, 001, '+201255556668'), 
(022, 002, '+201555556669'), 
(023, 003, '+201066667777'), 
(024, 004, '+201166667778'), 
(025, 005, '+201266667779'), 
(026, 006, '+201566667780'), 
(027, 007, '+201077778881'), 
(028, 008, '+201177778882'); 

-- View all the information in the Patient table
SELECT * FROM Patient;

-- View all the information in the Patient_Phone table
SELECT * FROM Patient_Phone;

-- Created DonationEvent table that manages all the donations' records
CREATE TABLE DonationEvent(
DonationID INT PRIMARY KEY NOT NULL,
DonorID INT NOT NULL,

-- DonorID is a foreign key from the Donor table that tells us which Donor we are dealing with
CONSTRAINT FK_Donor_Donation FOREIGN KEY (DonorID) REFERENCES Donor(DonorID) ON DELETE CASCADE,

BankID INT NOT NULL,

-- BankID is a foreign key from the BloodBank table that tells us which Blood Bank we are dealing with
CONSTRAINT FK_BankID_Donation FOREIGN KEY (BankID) REFERENCES BloodBank(BankID) ON DELETE CASCADE,

DonationDate DATE NOT NULL,
HemoglobinLevel FLOAT NOT NULL,
Weight FLOAT NOT NULL
);

-- We want to check if the Donor can legally donate by checking his/her age if it is in the legal range which is between 18 and 65
-- Also the checking the hemoglobin level if it is in the legal range which is more than 13.0 g/dL in males and 12.5 g/dL in females
-- using a DELIMITER which gets the hemoglobin level and calcualtes the age while inserting the info in the donation event
-- If any one of the age or the hemoglobin level is not in the legal range then it throws an error which tells us the problem we are facing
DELIMITER //

CREATE TRIGGER Validate_Donation_Requirements
BEFORE INSERT ON DonationEvent
FOR EACH ROW
BEGIN
    DECLARE Donor_Age INT;
    DECLARE Donor_Gender ENUM('Male','Female');

    -- Get donor info
    SELECT TIMESTAMPDIFF(YEAR, DateOfBirth, CURDATE()), Gender 
    INTO Donor_Age, Donor_Gender
    FROM Donor
    WHERE DonorID = NEW.DonorID;

    -- Check Age (18-65)
    IF Donor_Age < 18 OR Donor_Age > 65 THEN
        SIGNAL SQLSTATE '45000'
        SET MESSAGE_TEXT = 'Rejected: Donor must be 18-65 years old.';
    END IF;

    -- Check Hemoglobin (based on gender)
    IF (Donor_Gender = 'Male' AND NEW.HemoglobinLevel < 13.0) THEN
        SIGNAL SQLSTATE '45000'
        SET MESSAGE_TEXT = 'Rejected: Male hemoglobin must be at least 13.0 g/dL.';
    ELSEIF (Donor_Gender = 'Female' AND NEW.HemoglobinLevel < 12.5) THEN
        SIGNAL SQLSTATE '45000'
        SET MESSAGE_TEXT = 'Rejected: Female hemoglobin must be at least 12.5 g/dL.';
    END IF;
    
END //

DELIMITER ;


-- Insert Dontions' records to the table
INSERT INTO DonationEvent VALUE
(001, 002, 001, '1992-11-07', 24.2, 71.5),
(002, 001, 001, '2024-02-04', 13.6, 62.5),
(003, 001, 004, '2026-05-06', 22.1, 61.0),
(004, 003, 002, '2026-05-08', 21.0, 75.0),
(005, 004, 001, '2023-12-15', 14.5, 78.2),
(006, 005, 002, '2024-01-20', 13.8, 65.4),
(007, 006, 003, '2024-02-10', 15.2, 82.0),
(008, 007, 004, '2023-11-25', 15.9, 59.5),
(009, 008, 005, '2024-03-05', 14.1, 70.0),
(010, 009, 001, '2023-10-12', 13.5, 74.3),
(011, 010, 002, '2024-04-18', 16.0, 88.6),
(012, 012, 003, '2024-05-01', 14.8, 72.1),
(013, 012, 004, '2023-09-30', 13.2, 67.8),
(014, 013, 005, '2024-02-28', 15.5, 80.5),
(015, 014, 001, '2023-08-14', 14.2, 76.4),
(016, 015, 002, '2024-01-05', 13.9, 63.2),
(017, 016, 003, '2024-03-22', 15.7, 85.0),
(018, 017, 004, '2023-12-01', 13.8, 58.9),
(019, 018, 005, '2024-04-10', 14.6, 71.2),
(020, 019, 001, '2023-11-11', 13.4, 75.8),
(021, 020, 002, '2024-02-14', 15.1, 79.4),
(022, 021, 003, '2024-05-05', 14.0, 68.3),
(023, 022, 004, '2023-10-25', 13.7, 73.1),
(024, 023, 005, '2024-03-15', 15.9, 87.2),
(025, 024, 001, '2024-01-30', 14.4, 77.0),
(026, 025, 002, '2023-09-15', 13.1, 66.5),
(027, 026, 003, '2024-04-25', 15.3, 81.9),
(028, 027, 004, '2023-12-28', 13.7, 60.1),
(029, 028, 005, '2024-05-07', 14.9, 74.5);

-- View all the records in the DonationEvent table
SELECT * FROM DonationEvent;

-- Create the TransfusionRequest table with updated constraints.

CREATE TABLE TransfusionRequest(
RequestID INT NOT NULL,
PatientID INT NOT NULL,
HospitalID INT NOT NULL,
RequiredBloodType ENUM('A+', 'A-', 'B+', 'B-', 'AB+', 'AB-', 'O+', 'O-') NOT NULL,
UnitsRequired INT,
UrgencyLevel ENUM('Low', 'Medium', 'High', 'Critical') NOT NULL,
RequestDate DATE,
Status_of_Request ENUM('Pending', 'In Progress', 'Fulfilled', 'Cancelled') DEFAULT 'Pending',

-- Assign RequestID as Primary Key.
PRIMARY KEY (RequestID),

-- We have BankID , DonorID as Foreign Key.
CONSTRAINT FK_Hospital_Request FOREIGN KEY (HospitalID) 
	REFERENCES Hospital(HospitalID),
CONSTRAINT FK_Patient_Request FOREIGN KEY (PatientID, HospitalID) 
	REFERENCES Patient(PatientID, HospitalID),

-- Data Integrity: Ensure requested units is a positive number
CONSTRAINT chk_Unit_Number_Positive CHECK (UnitsRequired > 0)

);

-- Insert TransfusionRequests' information to the TransfusionRequest table
INSERT INTO TransfusionRequest VALUES
(001, 001, 001, 'A+', 2, 'High', '2026-05-01', 'Fulfilled'),
(002, 002, 002, 'O-', 1, 'Critical', '2026-05-02', 'Fulfilled'),
(003, 003, 003, 'B+', 3, 'Medium', '2026-05-03', 'In Progress'),
(004, 004, 004, 'AB-', 1, 'Low', '2026-05-03', 'Pending'),
(005, 005, 005, 'O+', 4, 'Critical', '2026-05-04', 'Fulfilled'),
(006, 006, 006, 'A-', 2, 'High', '2026-05-04', 'In Progress'),
(007, 007, 007, 'B-', 2, 'Medium', '2026-05-05', 'Cancelled'),
(008, 008, 008, 'AB+', 1, 'Low', '2026-05-05', 'Pending'),
(009, 009, 009, 'O-', 2, 'High', '2026-05-05', 'Fulfilled'),
(010, 010, 010, 'A+', 3, 'Critical', '2026-05-06', 'In Progress'),
(011, 011, 011, 'B+', 1, 'Medium', '2026-05-06', 'Fulfilled'),
(012, 012, 012, 'O+', 5, 'High', '2026-05-06', 'Pending'),
(013, 013, 013, 'A-', 1, 'Low', '2026-05-07', 'Pending'),
(014, 014, 014, 'AB-', 2, 'Critical', '2026-05-07', 'Fulfilled'),
(015, 015, 015, 'B-', 3, 'High', '2026-05-07', 'In Progress'),
(016, 016, 016, 'O+', 2, 'Medium', '2026-05-08', 'Pending'),
(017, 017, 017, 'A+', 1, 'Low', '2026-05-08', 'Cancelled'),
(018, 018, 018, 'AB+', 2, 'High', '2026-05-08', 'Pending'),
(019, 019, 019, 'O-', 4, 'Critical', '2026-05-08', 'In Progress'),
(020, 020, 020, 'B+', 2, 'Medium', '2026-05-08', 'Pending');

-- View all the information in the TransfusionRequest table
SELECT * FROM TransfusionRequest;

-- Create the TransfusionMatch table with updated constraints.
CREATE TABLE TransfusionMatch(
MatchID INT NOT NULL,
RequestID INT NOT NULL,
BankID INT NOT NULL,
UnitID INT NOT NULL,
MatchDate Date,
CompatibilityResult ENUM('Compatible', 'Incompatible', 'Pending') NOT NULL DEFAULT 'Pending',

PRIMARY KEY (MatchID),

CONSTRAINT FK_Transfusion_Request_Match FOREIGN KEY (RequestID) REFERENCES TransfusionRequest(RequestID) ON DELETE CASCADE,
CONSTRAINT FK_Blood_Unit_Match FOREIGN KEY (UnitID, BankID) REFERENCES BloodUnit(UnitID, BankID) ON DELETE CASCADE
);

INSERT INTO TransfusionMatch (MatchID, RequestID, BankID, UnitID, MatchDate, CompatibilityResult) VALUES
(001, 001, 001, 001, '2026-05-01', 'Compatible'),
(002, 002, 001, 002, '2026-05-01', 'Compatible'),
(003, 003, 002, 003, '2026-05-02', 'Incompatible'),
(004, 004, 002, 004, '2026-05-02', 'Pending'),
(005, 005, 003, 005, '2026-05-02', 'Compatible'),
(006, 006, 003, 006, '2026-05-03', 'Compatible'),
(007, 007, 004, 007, '2026-05-03', 'Incompatible'),
(008, 008, 004, 008, '2026-05-03', 'Pending'),
(009, 009, 005, 009, '2026-05-04', 'Compatible'),
(010, 010, 005, 010, '2026-05-04', 'Compatible'),
(011, 011, 001, 011, '2026-05-04', 'Incompatible'),
(012, 012, 001, 012, '2026-05-05', 'Pending'),
(013, 013, 002, 013, '2026-05-05', 'Compatible'),
(014, 014, 002, 014, '2026-05-05', 'Compatible'),
(015, 015, 003, 015, '2026-05-06', 'Incompatible'),
(016, 016, 003, 016, '2026-05-06', 'Pending'),
(017, 017, 004, 017, '2026-05-06', 'Compatible'),
(018, 018, 004, 018, '2026-05-07', 'Compatible'),
(019, 019, 005, 019, '2026-05-07', 'Incompatible'),
(020, 020, 005, 020, '2026-05-07', 'Pending');

SELECT * FROM TransfusionMatch;

SHOW TABLES;


SET FOREIGN_KEY_CHECKS = 0;

DROP TABLE Donor;
DROP TABLE Hospital;
DROP TABLE BloodBank;
DROP TABLE Patient;
DROP TABLE BloodInventory;
DROP TABLE BloodUnit;
DROP TABLE Bank_Phone;
DROP TABLE Hospital_Phone;
DROP TABLE Donor_Phone;
DROP TABLE Patient_Phone;
DROP TABLE DonationEvent;
DROP TABLE TransfusionRequest;
DROP TABLE TransfusionMatch;

TRUNCATE TABLE Donor;
TRUNCATE TABLE Hospital;
TRUNCATE TABLE BloodBank;
TRUNCATE TABLE Patient;
TRUNCATE TABLE BloodInventory;
TRUNCATE TABLE BloodUnit;
TRUNCATE TABLE Bank_Phone;
TRUNCATE TABLE Hospital_Phone;
TRUNCATE TABLE Donor_Phone;
TRUNCATE TABLE Patient_Phone;
TRUNCATE TABLE DonationEvent;
TRUNCATE TABLE TransfusionRequest;
TRUNCATE TABLE TransfusionMatch;
-- Also truncate Hospital table if you have one
SET FOREIGN_KEY_CHECKS = 1;

