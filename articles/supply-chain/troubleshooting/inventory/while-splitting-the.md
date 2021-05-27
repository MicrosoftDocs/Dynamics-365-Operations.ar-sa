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
ms.openlocfilehash: 185365ced5c4516d8fcdbdca88794d0078615888
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026244"
---
# <a name="when-a-catch-weight-quantity-is-split-minimum-quantity-is-used-instead-of-nominal-quantity"></a>عند تقسيم كمية وزن التعبئة، يتم استخدام الحد الأدنى للكمية بدلاً من الكمية الإسمية

رقم KB: 4612073

## <a name="symptoms"></a>العلامات

عند تقسيم كمية التعبئة إلى مجموعات، فإن الحقل **كمية الانتقاء** يستخدم الحد الأدنى من الكمية المعينة للصنف، وليس الكمية الإسمية.

## <a name="resolution"></a>الدقة

يعمل النظام كما هو مصمم. يستخدم النظام إعداد الحد الأدنى لكمية كل صنف للانتقاء.
