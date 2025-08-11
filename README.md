# IDA
Engineering Data Analytics with Python Case Study


### case_komponente.csv 用于 case study
1. 来自车辆表（Fahrzeuge_OEM1_Typ11.csv / Fahrzeuge_OEM1_Typ12.csv）
列名	含义
vehicle_id	车辆唯一标识符，例如 11-1-11-1
vehicle_production_date	车辆生产日期（出厂日期）
vehicle_manufacturer_no	车辆制造商编号
vehicle_plant_no	车辆工厂编号
vehicle_defective_flag	车辆是否有缺陷（0 = 否，1 = 是）
vehicle_defective_date	缺陷记录日期
vehicle_defective_mileage	缺陷记录时的车辆里程数（公里）

2. 来自注册信息表（Zulassungen_alle_Fahrzeuge.csv）
列名	含义
registration_municipality	登记车辆的城市/地区
registration_date	车辆首次登记（上牌）日期

3. 来自组件表（Komponente_K3AG1.csv，通过部件表间接关联）
列名	含义
component_production_date	K3AG1 变速箱组件的生产日期
component_manufacturer_no	变速箱组件的制造商编号
component_plant_no	变速箱组件的工厂编号
component_defective_flag	变速箱组件是否有缺陷（0 = 否，1 = 是）
component_defective_date	变速箱组件缺陷记录日期
component_defective_mileage	变速箱组件缺陷发生时的里程数（公里）


### Logistics_delay.csv 用于一般问题 task1，
字段名	含义
IDNummer	产品或组件唯一编号
Herstellernummer	生产厂商编号
Werksnummer	工厂编号
Produktionsdatum	生产日期（如果来源表中有）
IssueDate	出库日期 = 生产日期 + 1 天（假设生产后一天发货）
Wareneingang	接收日期（如果来源表中有）
LogisticsDelay_days	物流延迟天数 = 接收日期 - 出库日期（为正表示延迟，为负表示提前到货）