---
title: لا يمكن دمج إيصالات استلام منتجات متعددة في أمر شراء واحد
description: لا يمكنك دمج إيصالات استلام منتجات متعددة في أمر شراء واحد إذا كانت بنود إيصال استلام المنتجات المختلفة ذات تواريخ محاسبية مختلفة.
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
ms.openlocfilehash: 485306279281ceb55a140526f4216af35574af42
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475441"
---
# <a name="you-cant-consolidate-multiple-product-receipts-into-a-single-purchase-order"></a>لا يمكن دمج إيصالات استلام منتجات متعددة في أمر شراء واحد

## <a name="symptoms"></a>العلامات

لا يمكنك دمج إيصالات استلام منتجات متعددة في أمر شراء واحد إذا كانت بنود إيصال استلام المنتجات المختلفة ذات تواريخ محاسبية مختلفة.

## <a name="resolution"></a>الحل

في الإصدارات السابقة من Dynamics 365 Supply Chain Management، كان الدمج مسموحًا به في هذه الحالة. ومع ذلك، تعتبر الممارسة عرضة للخطأ. يجب ألا يختلف التاريخ المحاسبي في بنود أمر الشراء التي تم إنشاؤها عن التاريخ المحاسبي الموجود في بنود إيصال استلام المنتجات التي تم إنشاء بنود أمر الشراء منها. (يتطابق التاريخ المحاسبي على بنود أمر الشراء مع التاريخ المحاسبي على  رأس أمر  الشراء.) وبالتالي، لم يعد يُسمح بدمج إيصالات استلام متعددة في أمر شراء واحد.

يتم استخدام التاريخ المحاسبي، على سبيل المثال، لحجوزان الموازنة والالتزام بها. وبالتالي، يجب ان يتم الاحتفاظ بها أثناء الانتقال من إيصال استلام المنتجات إلى أمر الشراء.
