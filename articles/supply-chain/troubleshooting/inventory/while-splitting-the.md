---
title: عند تقسيم كمية وزن التعبئة، يتم استخدام الحد الأدنى للكمية بدلاً من الكمية الإسمية
description: عند تقسيم كمية التعبئة إلى مجموعات، فإن الحقل كمية الانتقاء يستخدم الحد الأدنى من الكمية المعينة للصنف، وليس الكمية الإسمية.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 424ad46281612f6a3e8cb4c90478a39f757d5416c3ce1d77ed6ff6dba7b20dcb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723445"
---
# <a name="when-a-catch-weight-quantity-is-split-minimum-quantity-is-used-instead-of-nominal-quantity"></a>عند تقسيم كمية وزن التعبئة، يتم استخدام الحد الأدنى للكمية بدلاً من الكمية الإسمية

رقم KB: 4612073

## <a name="symptoms"></a>العلامات

عند تقسيم كمية التعبئة إلى مجموعات، فإن الحقل **كمية الانتقاء** يستخدم الحد الأدنى من الكمية المعينة للصنف، وليس الكمية الإسمية.

## <a name="resolution"></a>الدقة

يعمل النظام كما هو مصمم. يستخدم النظام إعداد الحد الأدنى لكمية كل صنف للانتقاء.
