hello nodejs

  使用ssh方式 连接远程仓库

 1.生成本地电脑的 公钥和私钥
    ssh=keygen - t rsa -C "xxx@xx.com"
 1.1 将般地生成的公钥给写到远程的平台上(github)

2.将本地仓库与远程仓库建立py关系

    git remote add origgin xxx

    #添加
    - save 
    -insertOne
    -insertMany
    
    db.users.insertOne({name:'李思',age:29})
    db.test.insertMany([
        {
            name:'王五'
        },
        {
            name:'周六'
        }
    ])


    #删除

    -remove 
    -deleteOne
    -deleteMany
    db.users.remove({name:'张三'},{justOne:true})
#修改

    -save   如果传入了_id,那么save、会变成修改
    -updateOne
    -updateMany
db.users.save({name:'李思'})
db.test.update(
  {
    name:'张三'
  },
  {
      $set:{
          name:100
      }
  },
  {   upsert:true,
      multi:true
  }
)

db.users.find(
    {
        'title':'泰坦尼克号'
    }
)
db.users.find(
    {
        'title':/救/
    }
)

db.users.find({},{title:1},{_id:0})
#分页

总条数（totalSize）   11 个数据

每页显示5条 (pageSize) 5条

当前第几页(pageNum)  

一共多少页(totalPage)         Math.ceil(totalSize / pageSize)

1 . db.users.find().skip(0).limit(5);

2. db.users.find().skip(5).limit(5)

3. db.users.find().skip(5).limit(5)

公式 ：  db.users.find().skip((pageNum - )*pageSize).limit(pageSize)