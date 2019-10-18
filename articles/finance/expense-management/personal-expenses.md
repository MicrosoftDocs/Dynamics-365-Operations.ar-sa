---
title: النفقات الشخصية على تقرير نفقات
description: 'يشرح هذا الموضوع الأسلوبين المستخدمين لمعالجة المصروفات الشخصية للعامل في Microsoft Dynamics 365 Finance. '
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 825b6c131c8a65b99d5b7ebdadcd6389886f2d11
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176221"
---
# <a name="personal-expenses-on-an-expense-report"></a><span data-ttu-id="d5391-103">المصروفات الشخصية على تقرير المصروفات</span><span class="sxs-lookup"><span data-stu-id="d5391-103">Personal expenses on an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d5391-104">أثناء السفر من أجل العمل، قد يقوم العامل أحيانًا باستخدام بطاقة الائتمان الخاصة بالشركة لسداد مصروفاته الشخصية.</span><span class="sxs-lookup"><span data-stu-id="d5391-104">During business travel, workers might sometimes charge personal expenses to their corporate credit cards.</span></span> <span data-ttu-id="d5391-105">إذا لم تقم بتحديد آلية لمعالجة المصروفات الشخصية، فقد تتعطل عملية الموافقة على تقارير المصروفات عندما يُرسل العمال تقارير مصروفاتهم المفصلة.</span><span class="sxs-lookup"><span data-stu-id="d5391-105">If you don't define a process for handling personal expenses, the approval process for expense reports might be disrupted when workers submit their itemized expense reports.</span></span> 

<span data-ttu-id="d5391-106">هناك أسلوبان لمعالجة المصروفات الشخصية للعامل.</span><span class="sxs-lookup"><span data-stu-id="d5391-106">There are two methods for handling a worker's personal expenses:</span></span>

- <span data-ttu-id="d5391-107">**مدفوع بواسطة الموظف** - لا تدفع مؤسستك مصروفاتك الشخصية التي تظهر على الفاتورة الخاصة ببطاقة ائتمان الشركة.</span><span class="sxs-lookup"><span data-stu-id="d5391-107">**Paid by employee** – Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="d5391-108">بدلًا من ذلك، يقوم الموظف بإنشاء تقرير يعرض المصروفات الشخصية جنبًا إلى جنب مع مصروفات الشركة التي تم تحميلها على بطاقة ائتمان الشركة.</span><span class="sxs-lookup"><span data-stu-id="d5391-108">Instead, it creates a report that shows personal expenses together with the corporate expenses that were charged to the corporate credit card.</span></span>
- <span data-ttu-id="d5391-109">**مدفوع بواسطة الشركة** - تدفع مؤسستك الفاتورة كاملة من خلال بطاقة ائتمان الشركة، ثم تقوم بخصم المصروفات الشخصية من حساب العامل.</span><span class="sxs-lookup"><span data-stu-id="d5391-109">**Paid by company** – Your organization pays the whole bill for the corporate credit card and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="d5391-110">يمكنك تحديد الطريقة التي تستخدمها مؤسستك على صفحة **محددات إدارة المصروفات**.</span><span class="sxs-lookup"><span data-stu-id="d5391-110">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>
