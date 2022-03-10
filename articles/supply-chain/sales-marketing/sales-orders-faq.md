---
title: الاسئله المتداولة حول أوامر المبيعات
description: تتناول هذه الصفحة الأسئلة المتداولة التي يتم طرحها عند العمل مع أوامر المبيعات في Dynamics 365 Supply Chain Management.
author: Henrikan
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 3cee75b1d740e7cb414c674157dde0146e8faa50
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571607"
---
# <a name="sales-order-faqs"></a>الأسئلة المتداولة حول أمر مبيعات

تتناول هذه الصفحة الأسئلة المتداولة التي يتم طرحها عند العمل مع أوامر المبيعات في Dynamics 365 Supply Chain Management.

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a>هل يمكنني ربط أمر شراء  بأمر  مبيعات لتنفيذ الطلب؟

يمكنك إنشاء أمر شراء من أمر مبيعات. لمزيد من المعلومات، راجع [إنشاء أمر شراء من أمر مبيعات](/dynamics365/supply-chain/sales-marketing/tasks/create-purchase-order-sales-order).

## <a name="can-i-cancel-or-delete-a-sales-order-or-return-order"></a>هل يمكنني إلغاء أو حذف أمر مبيعات أو أمر إرجاع؟

يمكنك إلغاء أوامر الشراء وأوامر الإرجاع فقط عندما تكون حالتها *مُنشأة*. لمزيد من المعلومات، راجع [إلغاء أمر إرجاع](/dynamics365/supply-chain/service-management/cancel-return-order).

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a>هل يمكنني استعادة أمر مبيعات مفوتر تم حذفه؟

إذا تم حذف أمر مبيعات مفوتر عن طريق الخطأ، فيمكنك استعادته أو عرض تفاصيله.

انتقل إلى **حساب العميل \> الحركات \> المستند الأصلي \> عرض التفاصيل**. ابحث عن الفاتورة التي تبحث عنها وحددها لعرض تفاصيلها. تتضمن هذه التفاصيل مرجع أمر المبيعات. كما يجب أن تكون قادرًا على الوصول إلى تفاصيل أمر المبيعات من تلك الصفحة.

## <a name="how-do-i-delete-orphaned-sales-order-records"></a>كيف أحذف سجلات أوامر المبيعات المعزولة؟

لتنظيف سجلات أوامر المبيعات المعزولة ، قم بتشغيل الوظيفة الدورية *حذف أمر المبيعات* من خلال الانتقال إلى أي من الأماكن التالية:

- المبيعات والتسويق \> المهام الدورية \> تنظيف \> حذف أمر المبيعات
- البيع بالتجزئة والتجارة \> تكنولوجيا معلومات البيع بالتجزئة والتجارة \> تنظيف \> حذف أوامر المبيعات

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a>هل توجد طريقة لحساب العمولات على الفواتير التي تم ترحيلها؟

لا تدعم Supply Chain Management في الوقت الحالي حساب العمولات للفواتير المرحّلة.
