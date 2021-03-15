---
title: استكشاف أخطاء أوامر المبيعات وإصلاحها
description: يوضح هذا الموضوع كيفية إصلاح المشكلات التي قد تواجهها أثناء العمل مع أوامر المبيعات.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: c9a5b7a5e8cac7f8816233dd2d7ff1a7f84ea480
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974775"
---
# <a name="troubleshoot-sales-orders"></a>استكشاف أخطاء أوامر المبيعات وإصلاحها

يوضح هذا الموضوع كيفية إصلاح المشكلات التي قد تواجهها أثناء العمل مع أوامر المبيعات.

## <a name="the-tax-information-isnt-updated-if-i-change-the-location-on-a-sales-order-header"></a>لا يتم تحديث معلومات الضريبة عند تغيير الموقع على رأس أمر الشراء.

### <a name="issue-description"></a>وصف المشكلة

إذا تم تغيير عنوان الموقع أو المستودع أو عنوان التسليم على رأس امر المبيعات أو على مستوى البنود، فلن يتم تحديث معلومات ضريبة الحالة بشكل تلقائي للبنود.

### <a name="issue-resolution"></a>حل المشكلة

يتم هذا السلوك بسبب التصميم. تحدث المشكلة بسبب عدم تغيير عنوان التسليم والموقع والمستودع بشكل تلقائي على مستوى البنود. يجب تحديثها يدويًا.

## <a name="if-there-are-two-trade-agreements-for-the-same-period-or-overlapping-periods-the-same-agreement-line-is-always-selected"></a>عند وجود  اتفاقيتين  تجاريتين لنفس الفترة أو لفترات متراكبة، يتم دائمًا تحديد بند الاتفاقية نفسها.

### <a name="issue-description"></a>وصف المشكلة

إذا تم تحديد اتفاقيتين تجاريتين لنفس الفترة أو لفترات متراكبة، يتم دائمًا تحديد الاتفاقية التجارية نفسها في كل مرة عندما تنشئ بنود أمر مبيعات تحتوي على هذه الأصناف.‬

### <a name="issue-resolution"></a>حل المشكلة

عند وجود أكثر من اتفاقية تجارية واحد لتاريخ محدد، يتم دائمًا تحديد الاتفاقية التجارية ذات السعر الأقل. لمزيد من المعلومات، قم بتنزيل المستند التقني التالي: [الاتفاقيات التجارية في Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a>هل يمكنني ربط أمر شراء  بأمر  مبيعات لتنفيذ الطلب؟

يمكنك إنشاء أمر شراء من أمر مبيعات. لمزيد من المعلومات، راجع [إنشاء أمر شراء من أمر مبيعات](tasks/create-purchase-order-sales-order.md).

## <a name="i-cant-cancel-or-delete-a-return-order-or-a-sales-order"></a>لا يمكنني إلغاء أمر إرجاع أو أمر مبيعات أو حذفه.

يمكنك إلغاء أوامر الشراء وأوامر الإرجاع فقط عندما تكون حالتها *مُنشأة*. لمزيد من المعلومات، راجع [إلغاء أمر إرجاع](../service-management/cancel-return-order.md).

## <a name="when-i-try-to-cancel-a-sales-order-i-receive-a-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations-error"></a>عندما أحاول إلغاء أمر مبيعات أتلقى رسالة الخطأ " لا يمكن إزالة الحجوزات نظرًا لوجود عمل مُنشأ يعتمد على الحجوزات".‬

رمز الخطأ: WAX4661

إذا كان العمل يقترن بأمر مبيعات، فلا يمكنك إلغاء أمر المبيعات حتى يتم إلغاء العمل وعكسه. ينطبق هذا المتطلب حتى لون كان العمل المرتبط  بأمر  المبيعات مغلقا.

لإصلاح هذه المشكلة، اتبع هذه الخطوات.

1. قم بإلغاء العمل، وضع المخزون من جديد في الموقع المطلوب. انتقل إلى حمل العمل ذي الصلة لأمر المبيعات، وحدد **تقليل الكمية المنتقاة‬‏‫** على بند حمل العمل أو **إلغاء العمل** على جزء الإجراءات.

    أصبحت حالة العمل الآن *مُلغى*، ويتم إنشاء ومعالجة حركة المخزون الجديدة بشكل تلقائي لإعادة وضع المخزون في الموقع الذي ورد وصفه عند الإلغاء.

2. احذف حمل العمل. يتم أيضًا حذف الشحنة.
3. ينبغي الآن أن تكون قادرًا على الانتقال إلى أمر المبيعات وإلغائه.

## <a name="i-cant-cancel-an-intercompany-purchase-order-that-is-linked-to-a-sales-order"></a>لا يمكنني إلغاء أمر شراء بين الشركات الشقيقة يرتبط بأمر مبيعات.

### <a name="issue-description"></a>وصف المشكلة

إذا حاولت إلغاء أمر شراء بين الشركات الشقيقة يرتبط بأمر مبيعات، قد تتلقى رسالة الخطأ التالية "لا يمكن خفض الكمية بسبب تغيير علامة الكمية المحدثة المتبقية ".

### <a name="issue-resolution"></a>حل المشكلة

تم إصلاح هذه المشكلة في Microsoft Dynamics 365 Supply Chain Management الإصدار 10.0.13. في هذا الإصدار والإصدارات اللاحقة، يمكنك الآن إلغاء أمر الشراء بين الشركات الشقيقة المرتبط بأمر مبيعات.

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a>هل يمكنني استعادة أمر مبيعات مفوتر تم حذفه؟

### <a name="issue-description"></a>وصف المشكلة

تم حذف أمر مبيعات مفوتر عن طريق الخطأ، وترغب في استعادته أو عرض تفاصيله.

### <a name="issue-resolution"></a>حل المشكلة

إذا تمت فوترة أمر المبيعات المحذوف، فانتقل إلى **حساب العميل \> الحركات \> المستند الأصلي \> عرض التفاصيل**. ابحث عن الفاتورة التي تبحث عنها، وحددها لعرض تفاصيلها. تتضمن هذه التفاصيل مرجع أمر المبيعات. كما يجب أن تكون قادرًا على الوصول إلى تفاصيل أمر المبيعات من تلك الصفحة.

## <a name="the-deadline-of-a-sales-order-header-cant-be-found-in-the-salesorderheaderv2entity-data-entity"></a>يتعذر العثور على الموعد النهائي لرأس أمر المبيعات في كيان البيانات SalesOrderHeaderV2Entity

حقل الموعد النهائي غير موجود في الكيان *SalesOrderHeaderV2Entity*.

## <a name="i-must-delete-orphaned-sales-order-records"></a>يجب حذف سجلات أوامر المبيعات المعزولة.

لتنظيف سجلات أوامر المبيعات المعزولة ، قم بتشغيل الوظيفة الدورية *حذف أمر المبيعات* من خلال الانتقال إلى أي من الأماكن التالية:

- المبيعات والتسويق \> المهام الدورية \> تنظيف \> حذف أمر المبيعات
- البيع بالتجزئة والتجارة \> تكنولوجيا معلومات البيع بالتجزئة والتجارة \> تنظيف \> حذف أوامر المبيعات

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a>هل توجد طريقة لحساب العمولات على الفواتير التي تم ترحيلها؟

لا تدعم Supply Chain Management في الوقت الحالي حساب العمولات للفواتير المرحّلة.

## <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a>صنف المجموعة غير مدعوم في عملية بين الشركات الشقيقة.

لا يتوفر صنف المجموعة لأمر الشراء لأنك، إذا قمت بفحص بنود أمر المبيعات لصنف المجموعة، ستلاحظ أن الكمية هي *0* (صفر) والحالة هي *ملغى*. يتم هذا السلوك بسبب التصميم. يشتري أمر المبيعات مكونات صنف المجموعة فقط. ولا يشتري صنف المجموعة بحد ذاته.

إذا كان من الضروري شراء مجموعة، فعليك أن تأخذ في الاعتبار ما إذا كان يجب وضع علامة عليه كصنف مجموعة، لأن هذه الوظيفة مصممة بالفعل لسيناريوهات التعرف على الإيرادات. لمزيد من المعلومات حول أصناف المجموعة، راجع [المجموعات](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]