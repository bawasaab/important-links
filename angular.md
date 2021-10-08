#Angular Performance starts
--------------------------
https://medium.com/geekculture/the-complete-angular-performance-guide-for-2021-c5e55225b4d
https://medium.com/grapecity/angular-best-practices-for-2021-da9579bf5751

#Angular Performance ends
---------------------------

https://medium.com/swlh/angular-error-handling-and-logging-yet-another-story-d3e48ecaca55
https://medium.com/free-code-camp/best-practices-for-a-clean-and-performant-angular-application-288e7b39eb6f
https://medium.com/codex/multiple-interceptors-in-angular-e0880b2f7d91
http://joeljoseph.net/angular-6-deploy-on-apache-server-by-solving-404-not-found-error-on-page-refresh/
https://2019.stateofjs.com/front-end-frameworks/angular/

http://joeljoseph.net/angular-6-deploy-on-apache-server-by-solving-404-not-found-error-on-page-refresh/
http://jasonwatmore.com/post/2018/11/07/angular-7-reactive-forms-validation-example
https://codeburst.io/using-angular-route-guard-for-securing-routes-eabf5b86b4d1

http://jasonwatmore.com/post/2018/11/16/angular-7-jwt-authentication-example-tutorial
https://medium.com/@ryanchenkie_40935/angular-authentication-using-the-http-client-and-http-interceptors-2f9d1540eb8
https://stackoverflow.com/questions/53200399/angular-7-not-sending-correct-header-on-request
https://www.code-sample.com/2017/12/set-authorization-headers-angular-4-5.html
https://coryrylan.com/blog/creating-a-dynamic-checkbox-list-in-angular
https://stackoverflow.com/questions/55095745/angular-7-not-sending-header-on-request
https://stackoverflow.com/questions/39126638/ngmodel-cannot-be-used-to-register-form-controls-with-a-parent-formgroup-directi


ng build --prod --aot --base-href /straw-back/
ng build --prod --aot --base-href /straw-back-staging/


chrome://flags/#allow-insecure-localhost
https://medium.com/@saleemmalikraja/testing-service-workers-in-you-local-with-self-signed-certificate-angular-4f447c33d6fc

https://stackoverflow.com/questions/39632667/how-to-kill-the-process-currently-using-a-port-on-localhost-in-windows

Bootstrap not working properly in Angular 6
https://stackoverflow.com/questions/52676474/bootstrap-not-working-properly-in-angular-6/52676543

ng g module [module-name] --routing 
or 
ng g m [module-name] --routing



**********************************************************************************************************************************
angular httpclient send FORM-DATA
insertCoupon( in_data ):Observable<any>{

    let formData: FormData = new FormData(); 
    formData.append('coupon_name', in_data.coupon_name); 
    formData.append('coupon_code', in_data.coupon_code);
    
    return this.httpClient.post( 
      `${this.apiEndPoint}`, 
      formData,
      )
      .pipe(
        map((e:Response)=> e),
        catchError((e:Response)=> throwError(e))
      );
  }
**********************************************************************************************************************************

angular httpclient send x-www-form-urlencoded
insertCoupon( in_data ):Observable<any>{

    let body = new HttpParams()
    .set('coupon_name', in_data.coupon_name) 
    .set('coupon_code', in_data.coupon_code);
    
    return this.httpClient.post( 
      `${this.apiEndPoint}`, 
      body,
      )
      .pipe(
        map((e:Response)=> e),
        catchError((e:Response)=> throwError(e))
      );
  }
**********************************************************************************************************************************

