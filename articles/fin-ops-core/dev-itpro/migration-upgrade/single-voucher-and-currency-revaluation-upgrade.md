---
title: ترقية دفاتر يومية إيصال فردي وعمليات إعادة تقييم العملات
description: تُدخل بعض المؤسسات دفاتر يومية تحتوي على إيصال واحد يشتمل على أكثر من عميل أو مورد واحد، كما تُجري عملية إعادة تقييم العملة الأجنبية للحسابات المدينة أو الحسابات الدائنة. يصف هذا الموضوع الخطوات التي يجب على هذه المؤسسات اتباعها عند الترقية إلى الإصدار 1611 من Microsoft Dynamics 365 for Operations.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7c06e54c5be8d0a410b9f15f2a89def3076b4638
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681014"
---
# <a name="upgrade-single-voucher-journals-and-currency-revaluations"></a><span data-ttu-id="d9644-104">ترقية دفاتر يومية الإيصالات الفردية وعمليات إعادة تقييم العملة</span><span class="sxs-lookup"><span data-stu-id="d9644-104">Upgrade single-voucher journals and currency revaluations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d9644-105">تُدخل بعض المؤسسات دفاتر يومية تحتوي على إيصال واحد يشتمل على أكثر من عميل أو مورد واحد، كما تُجري عملية إعادة تقييم العملة الأجنبية للحسابات المدينة أو الحسابات الدائنة.</span><span class="sxs-lookup"><span data-stu-id="d9644-105">Some organizations enter journals that contain a single voucher that has more than one customer or vendor, and they also run the Accounts receivable or Accounts payable foreign currency revaluation process.</span></span> <span data-ttu-id="d9644-106">يصف هذا الموضوع الخطوات التي يجب على هذه المؤسسات اتباعها عند الترقية إلى الإصدار 1611 من Microsoft Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="d9644-106">This topic describes the steps that these organizations should follow when they upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

<span data-ttu-id="d9644-107">اتبع هذه الخطوات عند الترقية إلى الإصدار 1611 من Microsoft Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="d9644-107">Follow these steps when you upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

1.  <span data-ttu-id="d9644-108">قبل الترقية إلى Finance and Operations، شغّل عمليات إعادة تقييم العملة الأجنبية للحسابات المدينة والحسابات الدائنة.</span><span class="sxs-lookup"><span data-stu-id="d9644-108">Before you upgrade to Finance and Operations, run the foreign currency revaluation processes for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="d9644-109">عيّن الحقل **الطريقة** إلى **تاريخ الفاتورة**.</span><span class="sxs-lookup"><span data-stu-id="d9644-109">Set the **Method** field to **Invoice date**.</span></span> <span data-ttu-id="d9644-110">يتم إنشاء حركة إعادة تقييم تعكس عملية إعادة تقييم العملة الأجنبية الأخيرة.</span><span class="sxs-lookup"><span data-stu-id="d9644-110">A revaluation transaction is created that reverses the last foreign currency revaluation.</span></span> <span data-ttu-id="d9644-111">لذلك، يتم تقييم الحركات المفتوحة بعملة المحاسبة الأصلية الخاصة بها.</span><span class="sxs-lookup"><span data-stu-id="d9644-111">Therefore, the open transactions are valued at their original accounting currency.</span></span>
2.  <span data-ttu-id="d9644-112">الترقية إلى الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="d9644-112">Upgrade to version 1611.</span></span>
3.  <span data-ttu-id="d9644-113">أجرِ عمليات إعادة تقييم العملة الأجنبية للحسابات المدينة والحسابات الدائنة مرة ثانية.</span><span class="sxs-lookup"><span data-stu-id="d9644-113">Run the Accounts receivable and Accounts payable foreign currency revaluation processes again.</span></span> <span data-ttu-id="d9644-114">في هذه المرة، عيّن **الطريقة** إلى **القياسية**.</span><span class="sxs-lookup"><span data-stu-id="d9644-114">This time, set the **Method** field to **Standard**.</span></span> <span data-ttu-id="d9644-115">يتم إنشاء حركة إعادة تقييم جديدة استناداً إلى أسعار الصرف الحالية.</span><span class="sxs-lookup"><span data-stu-id="d9644-115">A new revaluation transaction is created that is based on the current exchange rates.</span></span> <span data-ttu-id="d9644-116">تسجل هذه الحركة الأرباح/الخسائر غير المحققة وحساب دفتر الأستاذ للملخص الصحيح.</span><span class="sxs-lookup"><span data-stu-id="d9644-116">This transaction records the unrealized gain/loss and the correct summary ledger account.</span></span>
