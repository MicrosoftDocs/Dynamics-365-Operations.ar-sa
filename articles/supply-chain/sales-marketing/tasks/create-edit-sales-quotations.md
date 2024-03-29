---
title: إنشاء عروض أسعار المبيعات وتحريرها
description: يوضح هذا الإجراء كيفية إنشاء عرض أسعار مبيعات وتحديثه.
author: Henrikan
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SalesQuotationTotals, SalesQuotationPriceSimulation, SalesQuotationEditLines, SrsReportViewerForm, smmSetNumSeqIfManual, CustTable, SalesTable, CustQuotationConfirmationJournal, CustQuotationJournal, CustSalesLines, SalesQuotationCopying, SalesQuotationDeleteQuotations, SalesQuotationListPagePreviewPane, SalesQuotationTypeGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1c409d294565f89eac95e42f6207573d22859100
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578934"
---
# <a name="create-and-edit-sales-quotations"></a>إنشاء عروض أسعار المبيعات وتحريرها

[!include [banner](../../includes/banner.md)]

يوضح هذا الإجراء كيفية إنشاء عرض أسعار مبيعات وتحديثه. يمكنك تنفيذ هذا الإجراء في البيانات الخاصة بك أو في شركة بيانات العرض التوضيحي USMF.


## <a name="create-a-sales-quotation"></a>إنشاء عرض أسعار مبيعات
1. انتقل إلى **جزء التنقل > الوحدات > المبيعات والتسويق > عروض أسعار المبيعات > كافة عروض الأسعار‬**.
2. انقر فوق **جديد**.
3. اكتب "عميل متوقع" في حقل **نوع الحساب**.
4. في الحقل **عميل متوقع**، أدخل قيمة أو حددها.
5. قم بتوسيع القسم **عام**. وحيث أنك اخترت إنشاء عرض أسعار من منطقة المبيعات والتسويق، سيتم تعيين النوع تلقائياً إلى عرض "أسعار المبيعات". لإنشاء عرض أسعار لمشروع، عليك الوصول إليه من الوحدة النمطية **إدارة المشاريع ومحاسبتها**.
6. انقر فوق **موافق**. تتشابه الحقول والإجراءات ببنود عرض الأسعار جداً مع تلك الموجودة في بنود أمر المبيعات.   وعلى غرار أوامر المبيعات، يمكنك إنشاء عروض أسعار لصنف معين، أو عندما يكون رقم الصنف مجهولًا أو غير موجود في وقت إنشاء عرض الأسعار، يمكنك إنشاء عروض أسعار لفئة مبيعات.     
7. في الحقل **الصنف**، أدخل قيمة أو حددها.
8. اكتب قيمة في الحقل **الموقع**.
9. في الحقل **الكمية**، أدخل رقمًا. إذا كان هناك اتفاقيات تجارية صالحة للصنف المحدد في البند، سيتم نسخ السعر والخصومات القابلة للتطبيق تلقائياً لبند عرض الأسعار. تأكد أن الحقل "سعر الوحدة" يحتوي على قيمة ويمكنك أيضًا إدخال قيم الخصم إذا أردت. 
10. انقر فوق **حفظ**.
11. في **جزء الإجراءات**، انقر فوق **عرض أسعار المبيعات**.
12. انقر فوق **الإجماليات**
13. انقر فوق **موافق**.
14. حدد بند عرض أسعار المبيعات.
15. في **جزء الإجراءات**، انقر فوق **عرض الأسعار**.
16. انقر فوق **محاكاة السعر**.
    - في الصفحة **تشغيل محاكاة السعر**، يمكنك إجراء تجربة ضبط الإيراد أو الربحية المتوقعة لعرض الأسعار على أساس سعر الوحدة أو مبلغ الخصم أو النسبة المئوية للخصم أو المبلغ الإجمالي أو الهامش أو هامش المساهمة المطلوب. عندما تكون راضيًا عن الأرقام المستهدفة، ستطبق الاقتراح على بند عرض الأسعار، وسيتم تحديث الحقول المتعلقة بسعره وفقا لذلك.  
    - يمكنك إنشاء العديد من عمليات محاكاة السعر كما تريد. عند النقر فوق **جديد**، يتم نسخ شروط السعر من بند عرض الأسعار الحالي إلى الصفحة. يمكنك بعد ذلك تعديل القيم في أي من المجالات المتعلقة بالأسعار إلى القيم المستهدفة. سوف يؤدي تغيير أحد الحقول إلى تشغيل إعادة الحساب في جميع الحقول الأخرى. لكي يحسب النظام هامش المبيعات ونسبة المساهمة، يجب أن تكون تكلفة وحدة المنتج معلومة. استخدم علامة التبويب "الأسعار التي تمت محاكاتها" للحصول على عرض مفصل للأسعار الأصلية والتغييرات المقترحة وأثرها على إجماليات عرض الأسعار. كقاعدة عامة، عندما يتم تطبيق محاكاة تحدد مبلغًا جديدًا لبند عرض الأسعار، سيعيد النظام الحساب ويدخل قيمة جديدة في الحقل "سعر الوحدة". إذا كانت المحاكاة مستندة إلى هامش جديد أو نسبة هامش مساهمة جديدة، سيتم تحديث الحقل "المبلغ الصافي" فقط، وستكون الحقل "سعر الوحدة" فارغاً. وفي كلتا الحالتين، سيتم حذف أية خصومات كانت في بند عرض الأسعار قبل إجراء المحاكاة.
17. في **جزء الإجراءات**، انقر فوق **عرض الأسعار**.
18. انقر فوق **إرسال عرض أسعار**.
19. حدد "نعم" في الحقل **طباعة عرض الأسعار**.
20. انقر فوق **موافق**. قد يستغرق التقرير دقيقة لإنشائه. لا تغلق الصفحة حتى تنشئَ التقرير.

## <a name="update-a-sales-quotation"></a>تحديث عرض أسعار مبيعات
1. انتقل إلى **جزء التنقل > الوحدات > المبيعات والتسويق > عروض أسعار المبيعات > كافة عروض الأسعار‬**.
2. في **جزء الإجراءات**، انقر فوق **متابعة**.
3. انقر فوق **تحويل إلى عميل**.
4. في الحقل **حساب العميل**، اكتب قيمة.
5. انقر فوق **تحقق**. تأكد من رؤية رسالة تفيد بأن رقم الحساب الذي قمت بكتابته مُتاح للاستخدام.  
6. انقر فوق **موافق**. أنشأ النظام الآن حساب عميل جديد للعميل المتوقع في عرض الأسعار.  
7. قم بإغلاق الصفحة.
8. في **جزء الإجراءات**، انقر فوق **متابعة**.
9. انقر فوق **تأكيد**.
10. في الحقل **السبب**، أدخل قيمة أو حددها.
11. انقر فوق **موافق**.
12. في **جزء الإجراءات**، انقر فوق **عام**.
13. انقر فوق **أوامر المبيعات**.
14. قم بإغلاق الصفحة.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]