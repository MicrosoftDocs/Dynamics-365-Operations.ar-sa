---
title: يتم استهلاك رقم إيصال استلام المنتجات حتى عند عدم إنشاء إيصال
description: يتم استهلاك رقم إيصال استلام المنتجات حتى في حالة عدم إنشاء إيصال مالي أثناء استلام المنتجات
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 0556969950c45e80d177a0e96096c4157d690ae3
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475466"
---
# <a name="a-product-receipt-voucher-number-is-consumed-even-when-not-generating-a-voucher"></a>يتم استهلاك رقم إيصال استلام المنتجات حتى عند عدم إنشاء إيصال

## <a name="symptoms"></a>العلامات

يتم استهلاك رقم إيصال استلام المنتجات حتى في حالة عدم إنشاء إيصال مالي اثناء استلام المنتجات.

## <a name="resolution"></a>الحل

إذا تم تعيين الخيار **استحقاق الالتزام على إيصال استلام المنتجات‬** إلى *لا* لمجموعة نماذج الأصناف، لن تحدث أي عمليات ترحيل لدفتر الأستاذ العام. ومع ذلك، سيتم تسجيل حدث فعلي لغرض المحاسبة في دفتر الأستاذ الفرعي، ويتطلب ذلك الحدث رقم إيصال. رقم الإيصال هذا هو رقم الإيصال الذي يُشار في حركات المخزون.

ننصحك بتعيين الخيار **استحقاق الالتزام على إيصال استلام المنتجات‬** إلى *نعم*، كما تم وصفه في منشور المدونة التالي: [ترحيل المصروفات المتنوعة عند استلام المنتجات](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).
