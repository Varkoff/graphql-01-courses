# graphql-01-courses

## Visualisez ce projet sur [CodeSandbox](https://codesandbox.io/s/ecstatic-cohen-suecg?file=/server2.js) !

### -> Queries :

```
query getCourses($topic: String) {
  courses(topic: $topic) {
    ...courseFields
  }
}

mutation changeTopic($courseID: Int!, $changedTopic: String!) {
  updateCourseTopic(id: $courseID, topic: $changedTopic) {
    ...courseFields
  }
}

query getCoursesWithString($str: String!) {
  coursesWithString(str: $str) {
    ...courseFields
  }
}

mutation createCourse($course: CourseInput) {
  createCourse(course: $course) {
    ...courseFields
  }
}

fragment courseFields on Course {
  id
  title
  author
  description
  topic
  url
}
```

### -> Query Variables

```
{
  "course": {
    "title": "Virgile aime Node.js !",
    "author": "Virgile RIETSCH"
  },
  "str": "Node.js",
	"courseID": 3,
  "changedTopic": "Angular"
}
```
