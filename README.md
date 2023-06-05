# Getting Started

1. yarn

2. yarn run deploy

3. yarn run start

4. Transaction behaviour in the 'before' handler error

-  tests/test.http -->
-   a. Update book,
-   b. Check log

   ==> Some changes from logBeforeBooksUpdate are committed

5. Transaction behaviour in the 'on' handler error
-   a. comment the code in srv/lib/common-service.ts, checksBeforeUpdate that rejects request
-   line 14 req.reject('Some before update error happened');
-   b. Uncomment the code in srv/lib/common-service.ts, checksBeforeUpdate that rejects request
-   line 35 // req.reject('Some ON update error happened');

-   tests/test.http -->
-   a.Clear log
-   b. Update book
-   c. Check log

   ==> No changes are committed

