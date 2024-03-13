router.get("/username/:username",async function (req,res)=>{

const regexPattern = new RegExp('^${req.params.username}' +'i' );
const data= await userModel.find({username:regexPattern});
res.json(data);


});