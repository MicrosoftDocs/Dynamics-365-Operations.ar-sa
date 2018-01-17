---
title: "محتوى Power BI - إدارة التحصيلات والائتمان"
description: "يوضح هذا الموضوع ما هو مدرج في محتوي Power BI - إدارة التحصيلات والائتمان. فهو يوضح كيفية الوصول إلى تقارير Power BI، ويوفر معلومات حول نموذج البيانات والكيانات التي يتم استخدامها لإنشاء المحتوى."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: aac6439bb54b3b9cab066b06c01763e880efef8e
ms.openlocfilehash: 694a8bfd4601b48a80872662fa7a16bf15d6e65c
ms.contentlocale: ar-sa
ms.lasthandoff: 12/18/2017

---

# <a name="credit-and-collections-management-power-bi-content"></a>محتوى Power BI - إدارة التحصيلات والائتمان

يوضح هذا الموضوع ما هو مدرج في محتوى Power BI **إدارة التحصيلات والائتمان**. فهو يوضح كيفية الوصول إلى تقارير Power BI، ويوفر معلومات حول نموذج البيانات والكيانات المستخدمة لإنشاء المحتوى.

## <a name="overview"></a>نظرة عامة

تم إنشاء محتوى Power BI **إدارة التحصيلات والائتمان** لمديري التحصيلات والائتمان، وموظفي التحصيلات. يوضح هذا الموضوع معايير الائتمان والتحصيلات الرئيسية، مثل أيام المبيعات المعلقة، والرصيد المتأخر، وتعريض الائتمان والعملاء الذين تجاوزوا الحد الائتماني الخاص بهم. يستخدم بيانات الحركة، ويوفر طرق عرض تجميعية للائتمان والتحصيلات في جميع الشركات. كما يوفر أيضًا تصنيف حسب الشركة، ومجموعة العميل، والعميل.

يتكون محتوى Power BI هذا من تقرير يتكون من 10 صفحات:

- صفحتان نظرة عامة (صفحة لنظرة عامة على الائتمان وصفحة واحدة لنظرة عامة على التحصيلات)
- ثم يلي ذلك 8 صفحات مفصلة توفر تفاصيل معايير الائتمان والتحصيلات المقسمة والمقطعة عبر أبعاد مختلفة

يتم عرض كافة المبالغ الموجودة بعملة النظام. يمكنك تعيين عملة النظام في صفحة **محددات النظام**.

بشكل افتراضي، يتم عرض بيانات الائتمان والتحصيلات للشركة الحالية. لمشاهدة البيانات في كافة أنحاء الشركات، قم بتعيين واجب **CustCollectionsBICrossCompany** للدور.

## <a name="accessing-the-power-bi-content"></a>الوصول إلى محتوى Power BI
يتم عرض محتوى Power BI **إدارة التحصيلات والائتمان** في مساحة العمل **تحصيلات وائتمان العميل**.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>التقارير المضمنة في محتوى Power BI

يتضمن محتوى Power BI **CustCollectionsBICrossCompany** تقريرًا يتكون من مجموعة من المقاييس. هذه المقاييس مرئية مثل المخططات والتجانبات والجداول. يوفر الجدول التالي نظرة عامة حول مجموعة المرئيات في محتوى Power BI لـ **CustCollectionsBICrossCompany**.

| صفحة التقرير                 | التصور |
|-----------------------------|---------------|
| نظرة عامة على التحصيلات        | <ul><li>العملاء الذين تجاوزوا تاريخ الاستحقاق</li><li>الحد الائتماني الزائد للعملاء</li><li>المستحقات على المبيعات اليومية 30 يومًا</li><li>الحالات المفتوحة</li><li>متوسط الأيام لإغلاق الحالة</li><li>الأنشطة المفتوحة</li><li>متوسط الأيام لإغلاق الأنشطة</li><li>إشعارات الفائدة المفتوحة</li><li>خطابات التحصيل المفتوحة</li><li>تعليق العميل</li><li>تعليق المبيعات</li><li>الأرصدة القديمة</li><li>مبالغ حالة التحصيلات</li><li>مبالغ كود التحصيلات</li><li>الشطب حسب السبب</li><li>الرصيد المستحق حسب المنطقة</li><li>المدفوعات المتوقعة</li></ul> |
| نظرة عامة حول الائتمان             | <ul><li>العملاء الذين تجاوزوا تاريخ الاستحقاق</li><li>الحد الائتماني مقابل الرصيد المستحق</li><li>شبكة الحد الائتماني الزائد للعملاء</li><li>العملاء فوق حد الائتمان لكل شركة</li><li>الائتمان المستخدم مقابل الحد الائتماني الإجمالي</li><li>الحد الائتماني مقابل الائتمان المستخدم حسب المنطقة</li><li>العملاء لكل تقدير ائتماني</li></ul> |
| حد ائتماني                | <ul><li>حد ائتماني</li><li>تفاصيل الحد الائتماني</li><li>الحد الائتماني حسب العميل</li><li>حد الائتمان لكل مجموعة عملاء</li><li>حد الائتمان لكل تقدير ائتماني لكل شركة</li><li>حد الائتمان مقابل الائتمان المستخدم حسب المنطقة</li></ul> |
| الحد الائتماني الزائد للعملاء | <ul><li>الحد الائتماني الزائد للعملاء</li><li>تفاصيل الحد الائتماني الزائد للعملاء</li><li>العملاء فوق حد الائتمان لكل شركة</li><li>الحد الائتماني الزائد للعميل لكل مجموعة عملاء</li><li>العملاء فوق حد الائتمان حسب المنطقة</li></ul> |
| العملاء الذين تجاوزوا تاريخ الاستحقاق          | <ul><li>العملاء الذين تجاوزوا تاريخ الاستحقاق</li><li>تفاصيل العملاء الذين تجاوزا تاريخ الاستحقاق</li><li>العملاء الذين تجاوزوا تاريخ الاستحقاق لكل شركة</li><li>العميل الذي تجاوز الاستحقاق لكل مجموعة عملاء</li><li>العميل الذي تجاوز تاريخ الاستحقاق حسب المنطقة</li></ul> |
| الأرصدة القديمة               | <ul><li>الأرصدة القديمة</li><li>تفاصيل الأرصدة المتقادمة</li><li>الأرصدة القديمة لكل شركة</li><li>الأرصدة القديمة لكل مجموعة عملاء</li></ul> |
| المدفوعات المتوقعة           | <ul><li>المدفوعات المتوقعة</li><li>تفاصيل المدفوعات المتوقعة</li><li>الدفعات المستحقة لكل شركة</li><li>الدفعات المتوقعة لكل مجموعة عملاء</li><li>الدفعات المتوقعة حسب المنطقة</li></ul> |
| عمليات الشطب                  | <ul><li>عمليات الشطب حسب المنطقة</li><li>تفاصيل عمليات الإلغاء</li><li>عمليات الإلغاء حسب الحساب الرئيسي</li><li>عمليات الإلغاء حسب الشركة</li><li>عمليات الإلغاء لكل مجموعة عملاء</li><li>عمليات الشطب حسب المنطقة</li></ul> |
| حالة المجموعات          | <ul><li>متنازع عليه</li><li>تم مخالفة التعهد بالسداد</li><li>تعهد بالسداد</li><li>تفاصيل حالة التحصيلات</li><li>مبالغ حالة التحصيلات</li><li>الحالات المفتوحة</li><li>الأنشطة المفتوحة</li></ul> |
| خطابات التحصيلات         | <ul><li>مبالغ كود التحصيل</li><li>تفاصيل مبلغ كود التحصيل</li><li>مبلغ خطاب التحصيل لكل شركة</li><li>مبلغ خطاب التحصيل لكل مجموعة العميل</li><li>مبلغ خطاب التحصيل حسب المنطقة</li></ul> |

يمكنك تصفية المخططات والإطارات المتجانبة الموجودة على كافة هذه التقارير وتثبيتها بلوحة المعلومات. لمزيد من المعلومات حول كيفية التصفية والتثبيت في Power BI، راجع [إنشاء لوحة معلومات وتكوينها](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). يمكنك أيضًا استخدام وظيفة تصدير البيانات الأساسية لتصدير البيانات الأساسية التي تم تلخيصها في المرئيات.

## <a name="understanding-the-data-model-and-entities"></a>فهم نموذج البيانات والكيانات

تُستخدم البيانات التالية لملء صفحات التقارير في محتوى Power BI **إدارة الائتمان والتحصيلات**. يتم تمثيل هذه البيانات كقياسات مجمعة تم تجهيزها في مخزن الكيانات. مخزن الكيانات هو قاعدة بيانات لخادم Microsoft SQL تم تحسينها للتحليلات. لمزيد من المعلومات، راجع [نظرة عامة عن تكامل Power BI مع متجر الكيان](../../dev-itpro/analytics/power-bi-integration-entity-store.md).

| الكيان                                      | القياسات التجميعية الرئيسية           | مصدر البيانات                                 | الحقل                                                      | ‏‏الوصف |
|---------------------------------------------|--------------------------------------|---------------------------------------------|------------------------------------------------------------|-------------|
| CustCollectionsBIActivitiesAverageCloseTime | NumOfActivities ،AveragecClosedTime  | smmActivities                               | AverageOfChildren(AverageClosedTime) Count(ActivityNumber) | عدد الأنشطة المتوقعة ومتوسط الوقت لإغلاق تلك الأنشطة. |
| CustCollectionsBIActivitiesOpen             | ActivityNumber                       | smmActivities                               | Count(ActivityNumber)                                      | عدد الأنشطة المفتوحة. |
| CustCollectionsBIAgedBalances               | AgedBalances                         | CustCollectionsBIAgedBalancesView           | Sum(SystemCurrencyBalance)                                 | مبلغ الأرصدة القديمة. |
| CustCollectionsBIBalancesDue                | SystemCurrencyAmount                 | CustCollectionsBIBalanceDueView             | Sum(SystemCurrencyAmount)                                  | المبالغ المتأخرة. |
| CustCollectionsBICaseAverageCloseTIme       | NumOfCases ،CaseAverageClosedTime    | CustCollectionsCaseDetail                   | AverageOfChildren(CaseAverageClosedTime) Count(NumOfCases) | عدد الحالات المتوقعة ومتوسط الوقت لإغلاق تلك الحالات. |
| CustCollectionsBICasesOpen                  | CaseId                               | CustCollectionsCaseDetail                   | Count(CaseId)                                              | عدد الحالات المفتوحة. |
| CustCollectionsBICollectionLetter           | CollectionLetterNum                  | CustCollectionLetterJour                    | Count(CollectionLetterNum)                                 | عدد خطابات التحصيل المفتوحة. |
| CustCollectionsBICollectionLetterAmount     | CollectionLetterAmounts              | CustCollectionsBIAccountsReceivables        | Sum(SystemCurrencyAmount)                                  | رصيد خطابات التحصيل المرحلة. |
| CustCollectionsBICollectionStatus           | CollectionStatusAmounts              | CustCollectionsBIAccountsReceivables        | Sum(SystemCurrencyAmount)                                  | رصيد الحركات مع حالة التحصيل. |
| CustCollectionsBICredit                     | CreditExposed، AmountOverCreditLimit | CustCollectionsBICreditView                 | Sum(CreditExposed), Sum(AmountOverCreditLimit)             | مبلغ تعرض الائتمان ومبالغ العملاء الذين تجاوزوا الحد الائتماني الخاص بهم. |
| CustCollectionsBICustOnHold                 | موقوف                              | CustCollectionsBICustTable                  | Count(Blocked)                                             | عدد العملاء قيد الانتظار. |
| CustCollectionsBIDSO                        | DSO30                                | CustCollectionsBIDSOView                    | AverageOfChildren(DSO30)                                   | أيام تحصيل المبيعات لـ 30 يومًا. |
| CustCollectionsBIExpectedPayment            | ExpectedPayment                      | CustCollectionsBIExpectedPaymentView        | Sum(SystemCurrencyAmounts)                                 | مجموع المدفوعات المتوقعة خلال العام التالي. |
| CustCollectionsBIInterestNote               | InterestNote                         | CustInterestJour                            | Count(InterestNote)                                        | عدد إشعارات الفائدة التي تم إنشاؤها. |
| CustCollectionsBISalesOnHold                | SalesId                              | SalesTable                                  | Count(SalesId)                                             | عدد إجمالي أوامر المبيعات قيد الانتظار. |
| CustCollectionsBIWriteOff                   | WriteOffAmount                       | CustCollectionsBIWriteOffView               | Sum(SystemCurrencyAmount)                                  | مجموع الحركات التي تم شطبها. |

