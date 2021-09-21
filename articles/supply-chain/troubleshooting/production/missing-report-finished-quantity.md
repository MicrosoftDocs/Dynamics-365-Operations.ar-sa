---
title: الإبلاغ عند فشل التحديث المنتهي مع ظهور خطأ في الكمية المفقودة
description: إذا حاولت إنهاء أمر إنتاج أثناء الإبلاغ عن كمية خطأ، ولكن ليس بشأن الوقت وكمية المادة، سوف يفشل الإبلاغ عن التحديث المنتهي.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 7785549c47063727f2749749940c1a96a351e70f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475443"
---
# <a name="report-as-finished-update-fails-with-a-missing-quantity-error"></a>الإبلاغ عند فشل التحديث المنتهي مع وجود خطأ في الكمية المفقودة

## <a name="symptoms"></a>العلامات

يمكنك الإبلاغ عن أمر إنتاج بأنه منته أثناء الإبلاغ عن كمية خطأ، ولكن ليس أثناء الإبلاغ عن الوقت أو كمية المادة. سيفشل التحديث الذي تم الإبلاغ عنه كمنته عند محاولة إنهاء أمر الإنتاج، وستتلقى رسالة الخطأ التالية:

> تقرير مفقود ككمية منتهية.

## <a name="resolution"></a>الحل

إذا أبلغت عن كمية خطأ في أمر إنتاج، فيجب أيضاً الإبلاغ عن الكمية الجيدة.
