public class University
{
    private List<Student> students;

    public University()
    {
        students = new List<Student>();
    }

    public void AddStudent(Student student)
    {
        students.Add(student);
    }
}

In this example, the `University` class aggregates `Student` objects. Students can exist independently of the university, and they can be added or removed from the university as needed.