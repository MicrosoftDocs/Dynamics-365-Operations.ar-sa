---
title: تم تحديد نفس الاتفاقية التجارية عند إنشاء بنود أمر المبيعات
description: عند وجود أكثر من اتفاقية تجارية واحدة محددة لتاريخ معينة، يتم دائمًا تحديد الاتفاقية التجارية ذات السعر الأقل عند إنشاء بنود أمر المبيعات.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a586a399fb349965b972191bec1271651bec5fcb
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475477"
---
# <a name="if-two-trade-agreements-exist-for-overlapping-dates-the-same-one-is-always-selected"></a>في حالة وجود اتفاقيات تجارة للتواريخ المتداخلة، يتم تحديد نفس الاتفاقية دائمًا

## <a name="symptoms"></a>العلامات

إذا تم تحديد اتفاقيتين تجاريتين لنفس الفترة أو لفترات متراكبة، يتم دائمًا تحديد الاتفاقية التجارية نفسها في كل مرة عند إنشاء بنود أمر مبيعات تحتوي على هذه الأصناف.‬

## <a name="resolution"></a>الحل

عند وجود أكثر من اتفاقية تجارية واحد لتاريخ محدد، يتم دائمًا تحديد الاتفاقية التجارية ذات السعر الأقل. لمزيد من المعلومات، قم بتنزيل المستند التقني التالي: [الاتفاقيات التجارية في Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).
