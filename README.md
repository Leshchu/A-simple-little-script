# A-simple-little-script
Protractor code
describe("iStock app", function() {

  it("This test will cover certain 'happy flow' included in Zadanie 1", function() 
		  { 
	  browser.get("https://www.istockphoto.com/pl");
	  
	  		  
	  element(by.className("account")).click();
	  
	  element(by.model("new_session['username']")).sendKeys("leshchu@mailinator.com");
	  
	  element(by.model("new_session['password']")).sendKeys("zaq123wsx");
	  
	  element(by.id("sign_in")).click();
	  
	  element(by.className("wide-header right-off-canvas-toggle-menu")).click();
	  
	  element(by.className("overview_container")).click();
	  
	  element(by.className("your-account")).click();
	  
	  element(by.partialLinkText('profile')).click();
	  
	  var span1 = element(by.binding('Twój nr klienta: 18642709'));
	  expect(span1.getText()).toEqual('Twój nr klienta: 18642709');
	  
	  element(by.model("profile['firstName']")).sendKeys("XXXXXXXX");
	  
	  element(by.id("update-button")).click();
	  
	  element(by.model("profile['firstName']")).sendKeys("YYYYY");
	  
	  element(by.id("update-button")).click();
	  
	  expect(Element(by.model("profile['firstName']")).getText()).toEqual("YYYYY");
	  
	  element(by.partialLinkText('profile')).click();
	  
	  browser.get("https://www.istockphoto.com/pl");
	  
	  element(by.className("your-non-default phrase")).sendKeys("hapinness");
	  
	  element(by.className("search-bar__submit")).click();
			  
	  browser.get("https://www.istockphoto.com/pl/zdj%C4%99cie/embracing-the-golden-autumn-gm869372160-144928361");
	  
	  element(by.className("ng-binding")).click();
	  
	  element(by.model("newBoardName")).sendKeys("new");
	  
	  element(by.className("button save")).click();
	  
	  
        });
  
  
   });
