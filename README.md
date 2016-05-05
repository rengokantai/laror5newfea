#### laror5newfea
#####2 imporvements
######Application record and application Job
rails5
```
module Act
  def do
  end
end

class ApplicationRecord < ActiveReocrd::Base
  self.abstract_class=true
  include Act
end
```
######Date and time
```
next_day prev_day
next_weekday prev_weekday
on_weekend? on_weekday?
next_week prev_week
Time.current.next_day
Time.current.next_week(:thursday)
Time.current.next_week(:thursday, :same_time=>true)
Time.days_in_year(2015)
```
#####3 Deprecations and Deletions
######Other deprecations and deletions
use
```
Relation.distinct
```
