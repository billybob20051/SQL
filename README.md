# SQL
Learning tools for SQL

table users {
  id int [pk, increment]
  username varchar
}
table comments {
  id int [pk, increment]
  contents varchar
  user_id int [ref: > users.id]
  post_id int [ref: > posts.id]
}
table posts {
  id int [pk, increment]
  title varchar
  }
