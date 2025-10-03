//Пример пользы инкапсуляции
package javaapplication1;
class Student { //Контроль целостности данных

    private int age;
    public void setAge(int age) {
        if (age >= 16 && age <= 100) {
            this.age = age;
        } else {
            throw new IllegalArgumentException("Возраст должен быть от 16 до 100 лет");
        }
    }
    public int getAge() {
        return age;
    }
}
public class JavaApplication1 {
    public static void main(String[] args) {
        Student student = new Student();
        student.setAge(20);
        System.out.println("Возраст: " + student.getAge());
    }
}
