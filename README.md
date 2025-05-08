# Create SpringBoot REST API That Returns List in JSON Format

First we create the java method that returns the list of students then we make that java method as a RESTful API by using Spring Annotations.


\springboot-rest-api\springboot-rest-api\src\main\java\net\javaguides\springboot\controller\StudentController.java


## Code Path

View code @

```diff
\springboot-rest-api\springboot-rest-api\src\main\java\net\javaguides\springboot\controller\StudentController.java
```

```bash
// http://localhost:8080/students
@GetMapping("students")
    public List<Student> getStudents(){
        List<Student> students = new ArrayList<>();
        students.add(new Student("Doe","John",1));
        students.add(new Student("John2", "Doe2", 2));
        students.add(new Student("Doe3", "John3", 3));
        students.add(new Student("Doe4","John4", 4));
        return students;
    }

```
