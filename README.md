node_mofuq
==============

node-mofuq is a simple task management tool by yaml.

Note
----

+ sample.yaml

```
- 
  name: 'task'
  progress: 15
- 
  name: 'taks2'
  progress: 70
  include: sample2.yaml
- 
  name: 'taks3'
  progress: 35
- 
  name: 'taks4'
  progress: 100
```

+ sample2.yaml

```
- 
  name: 'task'
  progress: 15
- 
  name: 'taks3'
  progress: 35
```


```
node bin/node-mofuq sample.yaml
```

```
[##________]    (015%)  [00h]   task
[#######___]    (070%)  [00h]   taks2
            [##________]    (015%)  [00h]   task
            [####______]    (035%)  [00h]   taks3
            tasks: 2
            hour: 0
            progress: 25%
[####______]    (035%)  [00h]   taks3
[##########]    (100%)  [00h]   taks4
tasks: 4
hour: 0
progress: 55%
```

## Installation

Run the following command

    $ npm install node_mofuq

Then to make sure the dependencies are installed:

    $ npm install

