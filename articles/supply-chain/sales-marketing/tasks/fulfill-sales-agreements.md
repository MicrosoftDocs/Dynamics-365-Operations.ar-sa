---
title: استيفاء اتفاقيات البيع
description: يوضح هذا الإجراء كيفية تنفيذ اتفاقية بيع عن طريق إقران أوامر المبيعات بها.
author: Henrikan
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreement, SalesAgreementGenerateReleaseOrder, SalesTableListPage, SalesTable, AgreementLine, SalesCreateOrder,  SalesEditLines, SalesAgreementHistory
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fe26d528e42da61d47fd2448e071bf9025c08f5d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573383"
---
# <a name="fulfill-sales-agreements"></a>استيفاء اتفاقيات البيع

[!include [banner](../../includes/banner.md)]

يوضح هذا الإجراء كيفية تنفيذ اتفاقية بيع عن طريق إقران أوامر المبيعات بها. يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF أو باستخدام بياناتك الخاصة. قبل تشغيل هذا الدليل، تأكد أن لديك اتفاقية بيع فعالة من نوع "التزام قيمة المنتج". وبدلاً من ذلك، يمكنك تشغيل دليل مهمة يسمى "إنشاء اتفاقيات البيع".  




## <a name="release-a-sales-order-from-the-agreement"></a>إصدار أمر مبيعات من الاتفاقية
1. انتقل إلى المبيعات والتسويق > اتفاقيات المبيعات > اتفاقية البيع.
2. في القائمة، حدد الاتفاقية التي تريد إصدار البند مقابلها.
3. في جزء الإجراءات، انقر فوق "اتفاقيات المبيعات".
4. انقر فوق "إصدار الأمر".
    * وكما يشير النص برأس صفحة "إنشاء أمر إصدار"، ستختلف التفاصيل المطلوبة لبنود أمر المبيعات تبعاً لما إذا كانت الاتفاقية على أساس الكمية أو القيمة.  
    * الاتفاقية الواردة في هذا الدليل من النوع "الالتزام بقيمة المنتج". وهذا سبب فراغ قسم البنود بهذه الصفحة. إذا كان الالتزام استند إلى كمية، فقد يتم نسخ معلومات البنود من الاتفاقية.  
5. انقر فوق "إنشاء".
    * تُعلمك الرسالة أنه تم إنشاء أمر الشراء. وحيث إن الأمر لا يتضمن أية بنود، يجب إضافة تفاصيل بند أمر لإكمال عملية الإصدار.   
6. قم بإغلاق الصفحة.
7. قم بإغلاق الصفحة.
8. انتقل إلى المبيعات والتسويق > أوامر المبيعات > كافة أوامر المبيعات.
9. في القائمة، ابحث عن الأمر الذي تم إنشاؤه كنتيجة إصدار أمر بالمهمة السابقة ثم افتحه.
10. انقر فوق "إضافة بند".
11. في الحقل "رقم الصنف"، انقر فوق زر القائمة المنسدلة لفتح البحث.
12. في الحقل "رقم الصنف"، اكتب الصنف المحدد في اتفاقية البيع المقترنة أو حدده.
13. في حقل الكمية، أدخل رقمًا.
    * تأكد من إدخال كمية الذي تضع المبلغ الصافي أقل من قيمة اتفاقية البيع المرتبطة به.  
    * لاحظ أنه بسبب ربط أمر المبيعات بالاتفاقية، يتم تطبيق النسبة المئوية للخصم على بند الأمر.  
14. انقر فوق "تحديث البند".
15. انقر فوق "تم الإرفاق".
    * تعرض الصفحة "الاتفاقية المرفقة" معرف وشروط الاتفاقية التي يتم إصدار البنود منها.  
16. قم بإغلاق الصفحة.
17. في جزء "الإجراءات"، انقر فوق "عام".
18. انقر فوق "اتفاقية البيع المرفقة".
19. قم بتوسيع قسم "تفاصيل البند".
20. انقر فوق علامة التبويب "التنفيذ".
    * تعرض علامة التبويب "التنفيذ" ملخصاً لجميع بنود أمر المبيعات المقترنة بهذا الالتزام وحالة التنفيذ لها بالإضافة إلى المبلغ أو الكمية التي لم يتم إصدارها بعد.   
21. قم بإغلاق الصفحة.
22. قم بإغلاق الصفحة.
23. قم بإغلاق الصفحة.

## <a name="apply-sales-agreement-in-the-order-process"></a>تطبيق اتفاقيات البيع في عملية الطلب
1. انتقل إلى المبيعات والتسويق > أوامر المبيعات > كافة أوامر المبيعات.
2. انقر فوق "جديد".
3. في الحقل "حساب العميل"، انقر فوق زر القائمة المنسدلة لفتح البحث.
4. في القائمة، ابحث عن العميل المحدد في اتفاقية البيع وحدده.
5. في القائمة، انقر فوق الارتباط في الصف المحدد.
6. قم بتوسيع القسم "عام".
7. في الحقل "معرف اتفاقية البيع"، انقر فوق زر القائمة المنسدلة لفتح البحث.
8. في القائمة، انقر فوق الارتباط في الصف المحدد.
9. انقر فوق نعم.
10. انقر فوق "موافق".
11. في القائمة، قم بوضع علامة للصف المحدد.
12. في الحقل "رقم الصنف"، انقر فوق زر القائمة المنسدلة لفتح البحث.
13. في الحقل "رقم الصنف"، اكتب الصنف المحدد في اتفاقية البيع المقترنة أو حدده.
14. في القائمة، انقر فوق الارتباط في الصف المحدد.
15. انقر فوق حفظ.
16. في "جزء الإجراءات"، انقر فوق "انتقاء وتعبئة‬".
17. انقر فوق "ترحيل إيصال التعبئة".
18. وسّع مقطع "المحددات".
19. حدد "نعم" في الحقل "الترحيل".
20. انقر فوق "موافق".
21. انقر فوق "موافق".
22. في جزء "الإجراءات"، انقر فوق "عام".
23. انقر فوق "اتفاقية البيع المرفقة".
24. انقر فوق علامة التبويب "التنفيذ".



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]