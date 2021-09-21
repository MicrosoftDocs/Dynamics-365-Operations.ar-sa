---
title: لا يمكنك حذف منتج تم إصداره
description: يمكنك حذف منتج تم إصداره وجميع متغيراته فقط إذا لم يكن للمنتج الذي تم إصداره إيه حركات مرتبطة.
author: SmithaNataraj
ms.date: 06/11/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2f03d45a36401314a4b02ff354fabb474568c48b
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475504"
---
# <a name="you-cant-delete-a-released-product"></a>لا يمكنك حذف منتج تم إصداره

## <a name="symptoms"></a>العلامات

يمكنك حذف منتج تم إصداره وجميع متغيراته فقط إذا لم يكن للمنتج الذي تم إصداره إيه حركات مرتبطة.

## <a name="resolution"></a>الحل

اتبع الخطوات التالية لحذف منتج أو أصل منتج تم إصداره.

1. يستخدم لإغلاق كافة الحركات المفتوحة للأصناف.
1. تقليل المخزون إلى 0 (صفر).
1. اجراء اقفال المخزون.
1. قم بحذف كافة متغيرات المنتج لأصل المنتج الذي تريد حذفه.
