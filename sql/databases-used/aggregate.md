# Aggregate

#### **`Database 1:`**

#### **`i) employees` Table**

<table><thead><tr><th>employee_id</th><th width="94">name</th><th>age</th><th width="130">department</th><th>salary</th><th>manager_id</th></tr></thead><tbody><tr><td>101</td><td>Alice</td><td>30</td><td>HR</td><td>60000.00</td><td>Null</td></tr><tr><td>102</td><td>Bob</td><td>28</td><td>IT</td><td>70000.00</td><td>101</td></tr><tr><td>103</td><td>Charlie</td><td>35</td><td>Finance</td><td>90000.00</td><td>101</td></tr><tr><td>104</td><td>David</td><td>40</td><td>IT</td><td>85000.00</td><td>102</td></tr><tr><td>105</td><td>Emma</td><td>25</td><td>Marketing</td><td>50000.00</td><td></td></tr><tr><td>106</td><td>Frank</td><td>32</td><td>HR</td><td>65000.00</td><td></td></tr><tr><td>107</td><td>Grace</td><td>29</td><td>Finance</td><td>95000.00</td><td></td></tr><tr><td>108</td><td>Hannah</td><td>38</td><td>IT</td><td>78000.00</td><td></td></tr></tbody></table>

#### **`ii) departments` Table**

| department\_id | department | location      |
| -------------- | ---------- | ------------- |
| 1              | HR         | New York      |
| 2              | IT         | San Francisco |
| 3              | Finance    | Chicago       |
| 4              | Marketing  | Los Angeles   |

**iii)  salaries table**

<table><thead><tr><th>salary_id</th><th width="100">employee_id</th><th>salary_amount</th><th>salary_date</th><th>bonus</th></tr></thead><tbody><tr><td>1</td><td>101</td><td>60000</td><td>2024-01-01</td><td>5000</td></tr><tr><td>2</td><td>102</td><td>70000</td><td>2024-01-01</td><td>3000</td></tr><tr><td>3</td><td>103</td><td>90000</td><td>2024-01-01</td><td>7000</td></tr><tr><td>4</td><td>104</td><td>85000</td><td>2024-01-01</td><td>6000</td></tr><tr><td>5</td><td>105</td><td>50000</td><td>2024-01-01</td><td>2000</td></tr><tr><td>6</td><td>106</td><td>65000</td><td>2024-01-01</td><td>4000</td></tr><tr><td>7</td><td>107</td><td>95000</td><td>2024-01-01</td><td>8000</td></tr><tr><td>8</td><td>108</td><td>78000</td><td>2024-01-01</td><td>5500</td></tr></tbody></table>
