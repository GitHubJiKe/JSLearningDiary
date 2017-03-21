#  day 1

## nodeJS->convertPDFToPicture

### tools (brew install behind tool lib)
*  pdftk
*  imagemagick
*  ghostscript

### node child_process.exec

	var exec = require('child_process').exec;
	var path = require('path');
	const picPath = '../pics/';
	
	function convertPDFToPic(pdfPath,picName,picType,cb){
	    picType = picType?picType:'png';
	    var _pdfPath = path.join(__dirname,pdfPath);
	    var _picPath = path.join(__dirname,picPath);
	    var bashStr = 'convert -density 150 ' + _pdfPath+' '+_picPath+picName+'.'+picType;
	    exec(bashStr,(err,stdout,stderr)=>{
	        cb(err,stdout);
	    });
	}
	
	
	exports.convertPDFToPic =convertPDFToPic;
	
	convertPDFToPic('../pdfs/test.pdf','test','png',(err,result)=>{
	    console.log(err,result);
	});
	
### with bash to convert

    **convert XXX.pdf XXX.png**