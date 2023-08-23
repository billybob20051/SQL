# SQL
Learning tools for SQL

table users {
  id serial [pk, increment]
  created_at timestamp
  updated_at timestamp
  username varchar(30)
}

table posts {
  id serial [pk, increment]
  created_at timestamp
  updated_at timestamp
  url varchar(200)
  user_id integer [ref: > users.id]
  caption varchar(240)
  lat real 
  lng real
}

table comments {
  id serial [pk, increment]
  created_at timestamp
  updated_at timestamp
  contents varchar(240)
  user_id integer [ref: > users.id]
  post_id integer [ref: > posts.id]
}

table likes {
  id serial [pk,increment]
  created_at timestamp
  user_id integer [ref: > users.id]
  comment_id integer [ref: > comments.id]
  post_id integer [ref: > posts.id]
}
