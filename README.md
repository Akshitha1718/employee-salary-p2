def get_employee_details():
    name = input("Enter Employee Name: ")
    emp_id = input("Enter Employee ID:")
    deparment = input("Enter Department:")
    basic_salary = float(input("Enter Basic Salary:"))
    return name,emp_id,deparment,basic_salary

def calculate_salary(basic_salary):
    hra = basic_salary*0.20
    da = basic_salary*0.10
    pf = basic_salary*0.12

    gross_salary = basic_salary+hra+da
    net_salary = gross_salary-pf
    return hra,da,pf,gross_salary,net_salary

def print_salary_slip(name,emp_id,department,basic,hra,da,pf,gross,net):
    print("\n===================EMPLOYEE SALARY SLIP==================")
    print("Employee Nmae :",name)
    print("Employee ID :",emp_id)
    print("Department :",department)
    print("--------------------------------")
    print("Basic Salary :Rs.",basic)
    print("HRA(20%) :Rs.",hra)
    print("DA(10%) :Rs.",da)
    print("PF Deduction :Rs.",pf)
    print("--------------------------------")
    print("Gross Salary :Rs.",gross)
    print("Net Salary :Rs.",net)
    print("=====================================================")
name, emp_id, department, basic = get_employee_details()
hra, da, pf, gross, net = calculate_salary(basic)
print_salary_slip(name, emp_id, department, basic, hra, da, pf, gross, net)
 

OUTPUT

Enter Employee Name: kathir
Enter Employee ID:1718
Enter Department:buisness
Enter Basic Salary:500000

===================EMPLOYEE SALARY SLIP==================
Employee Nmae : kathir
Employee ID : 1718
Department : buisness
--------------------------------
Basic Salary :Rs. 500000.0
HRA(20%) :Rs. 100000.0
DA(10%) :Rs. 50000.0
PF Deduction :Rs. 60000.0
--------------------------------
Gross Salary :Rs. 650000.0
Net Salary :Rs. 590000.0
=====================================================
