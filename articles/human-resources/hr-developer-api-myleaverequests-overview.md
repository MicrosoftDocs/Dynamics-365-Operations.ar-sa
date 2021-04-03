---
title: نظره عامة على MyLeaveRequests
description: يوفر كيان MyLeaveRequests في Microsoft Dynamics 365 Human Resources قائمة بطلبات الإجازات في النظام، مقيدة (محدودة) على الطلبات التي يمكن الوصول إليها للمستخدم الحالي الذي يقوم بالاستعلام عن الكيان.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c2c14a0cc935ad166a2c6600f1e96c3e09ab16ca
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465500"
---
# <a name="myleaverequests-overview"></a>نظره عامة على MyLeaveRequests

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يوفر كيان MyLeaveRequests في Microsoft Dynamics 365 Human Resources قائمة بطلبات الإجازات في النظام، مقيدة (محدودة) على الطلبات التي يمكن الوصول إليها للمستخدم الحالي الذي يقوم بالاستعلام عن الكيان.

## <a name="key"></a>مفتاح

  | اسم الخاصية | نوع البيانات |
  |---------------|-----------|
  | dataAreaId    | سلسلة    |
  | RequestId     | سلسلة    |
  | LeaveType     | سلسلة    |
  | LeaveDate     | التاريخ      |
  
## <a name="properties"></a>خصائص

  | اسم الخاصية     | نوع البيانات | مطلوب |
  |-------------------|-----------|----------|
  | dataAreaId        | سلسلة    | س        |
  | RequestId         | سلسلة    | س        |
  | LeaveType         | سلسلة    | س        |
  | LeaveDate         | التاريخ      | س        |
  | ReasonCodeId      | سلسلة    |          |
  | PersonnelNumber   | سلسلة    | س        |
  | RequestDate       | التاريخ      | س        |
  | تعليق           | سلسلة    |          |
  | الحالة            | تعداد      | س        |
  | ‏‏المقدار            | حقيقي      |          |
  | HalfDayDefinition | تعداد      |          |

## <a name="actions"></a>إجراءات

 | اسم الإجراء                               | ‏‏الوصف                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [إرسال](hr-developer-api-myleaverequests-submit.md)   | أرسل الطلب لمعالجته من خلال سير العمل. |

## <a name="see-also"></a>راجع أيضًا

- [إرسال طلب إجازة إلى سير العمل](hr-developer-api-myleaverequests-submit.md)
- [المصادقة](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]