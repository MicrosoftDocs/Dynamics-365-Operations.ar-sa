## <a name="main-account-to-msdyn_mainaccounts"></a>الحساب الرئيسي إلى msdyn_mainaccounts

يقوم هذا القالب بمزامنة البيانات بين تطبيقات Finance and Operations وCommon Data Service.

حقل Finance and Operations | نوع التعيين | حقل Dynamics 365 الآخر | القيمة الافتراضية
---|---|---|---
MAINACCOUNTID | = | msdyn_accountnumber | 
CHARTOFACCOUNTS | = | msdyn_chartofaccounts.msdyn_name | 
الاسم | = | msdyn_name | 
BALANCECONTROL | >< | msdyn_balancecontrol | 
EXCHANGEADJUSTMENTRATETYPE | = | msdyn_exchangeadjustmentratetype.msdyn_name | 
الإقفال | >< | msdyn_closing | 
REPORTINGEXCHANGEADJUSTMENTRATETYPE | = | msdyn_reportingexchangeadjustmentratetype.msdyn_name | 
DEBITCREDITREQUIREMENT | >< | msdyn_debitcreditrequirement | 
FINANCIALREPORTINGEXCHANGERATETYPE | = | msdyn_financialreportingexchangeratetype.msdyn_name | 
FOREIGNCURRENCYREVALUATION | >< | msdyn_foreigncurrencyrevaluation | 
MAINACCOUNTCATEGORY | = | msdyn_mainaccountcategoryname | 
MANDATORYPAYMENTREFERENCE | >< | msdyn_mandatorypaymentreference | 
مبالغ نقدية | >< | msdyn_monetary | 
OFFSETACCOUNTDISPLAYVALUE | = | msdyn_offsetaccount | 
POSTINGTYPE | >< | msdyn_postingtype | 
SRUCODE | = | msdyn_srucode | 
VALIDATECURRENCY | >< | msdyn_validatecurrencycode | 
VALIDATEUSER | >< | msdyn_validateuser | 
DEBITCREDITDEFAULT | >< | msdyn_debitcreditdefault | 
DEFAULTCURRENCY | = | msdyn_defaultcurrency.isocurrencycode | 
MAINACCOUNTTYPE | >< | msdyn_mainaccounttype | 
FINANCIALREPORTINGCURRENCYTRANSLATIONTYPE | >< | msdyn_financialreportingcurrencytrantype | 
المستخدم | = | msdyn_user | 
VALIDATEPOSTINGTYPE | >< | msdyn_validateposting | 
