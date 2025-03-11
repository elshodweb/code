# code
```
function getManagers(employees, employeeId) {
    let result = [];
    let employeeMap = new Map();

    
    for (let emp of employees) {
        employeeMap.set(emp.employeeId, emp.managerId);
    }

    
    while (employeeMap.has(employeeId)) {
        let managerId = employeeMap.get(employeeId);
        result.push(managerId);

       
        if (managerId === employeeId) break;

       
        employeeId = managerId;
    }

    return result;
}

```
