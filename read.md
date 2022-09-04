mongod --port 27017 --dbpath C:\MongoDB\data\db
mongo
> use my-blog
switched to db my-blog
> db.articles.insert([{
... name: 'learn-react',
... upvotes: 0,
... comments: [],
... }, {
... name: 'learn-node',
... upvotes: 0,
... comments: [],
... }, {
... name: 'my-thoughts-on-resumes',
... upvotes: 0,
... comments: [],
... }])
BulkWriteResult({
        "writeErrors" : [ ],
        "writeConcernErrors" : [ ],
        "nInserted" : 3,
        "nUpserted" : 0,
        "nMatched" : 0,
        "nModified" : 0,
        "nRemoved" : 0,
        "upserted" : [ ]
})
> db.articles.find({})
{ "_id" : ObjectId("630f39c766de2d1b89d3a348"), "name" : "learn-react", "upvotes" : 0, "comments" : [ ] }
{ "_id" : ObjectId("630f39c766de2d1b89d3a349"), "name" : "learn-node", "upvotes" : 0, "comments" : [ ] }
{ "_id" : ObjectId("630f39c766de2d1b89d3a34a"), "name" : "my-thoughts-on-resumes", "upvotes" : 0, "comments" : [ ] }
> db.articles.find({}).pretty()
{
        "_id" : ObjectId("630f39c766de2d1b89d3a348"),
        "name" : "learn-react",
        "upvotes" : 0,
        "comments" : [ ]
}
{
        "_id" : ObjectId("630f39c766de2d1b89d3a349"),
        "name" : "learn-node",
        "upvotes" : 0,
        "comments" : [ ]
}
{
        "_id" : ObjectId("630f39c766de2d1b89d3a34a"),
        "name" : "my-thoughts-on-resumes",
        "upvotes" : 0,
        "comments" : [ ]
}
> db.articles.find({name: 'learn-react'}).pretty()
{
        "_id" : ObjectId("630f39c766de2d1b89d3a348"),
        "name" : "learn-react",
        "upvotes" : 0,
        "comments" : [ ]
}
> db.articles.findOne({name: 'learn-react'})
{
        "_id" : ObjectId("630f39c766de2d1b89d3a348"),
        "name" : "learn-react",
        "upvotes" : 0,
        "comments" : [ ]
}
>
