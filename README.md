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

######Changes to parameters
```
params.to_unsafe_h.slice(:sort_by, :sort_dir)
```
Or
```
params.permit([:sort_by, :sort_dir])
params.slice(:sort_by, :sort_dir)
```
in rails 5:
```
hash={:a=>a,:b=>b}
obj=ActionController::Parameters#new(hash)
if(params==obj){}
```
###### Enumeratable#without
```
arr=[1,2,3]
arr.without(1)  #[2,3]
```
###### Enumeratable#pluck
```
arr=[{:a=>1,:b=>2},{:a=>3,:b=>4}]
arr.pluck(:b)  # [3,4]
```
######ArrayInquirer
```
roles=ActiveSupport::ArrayInquirer.new(array)
roles.class  # ActiveSupport::ArrayInquirer
```
```
arr=[...]
roles=arr.inquiry
role.class  # ActiveSupport::ArrayInquirer
```

```
roles=[1,2,3].inquiry
roles.1?  #true
```

#####3 Deprecations and Deletions
######Other deprecations and deletions
use
```
Relation.distinct
```
