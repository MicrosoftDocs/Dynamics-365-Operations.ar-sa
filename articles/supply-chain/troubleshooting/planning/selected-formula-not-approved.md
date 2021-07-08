---
title: لم تتم الموافقة على رقم المعادلة المحدد لأمر الدفعة
description: عند محاولة تأكيد أمر مخطط، تتلقى رسالة خطأ تنص على عدم الموافقة على رقم المعادلة المحدد لأمر دفعي.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4f993c92ca0a2f8f79e4b0e0eda43904529163f8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/22/2021
ms.locfileid: "6293998"
---
# <a name="selected-formula-number-isnt-approved-for-a-batch-order"></a><span data-ttu-id="462b5-103">لم تتم الموافقة على رقم المعادلة المحدد لأمر الدفعة</span><span class="sxs-lookup"><span data-stu-id="462b5-103">Selected formula number isn't approved for a batch order</span></span>

<span data-ttu-id="462b5-104">رمز الخطأ: PRO2614</span><span class="sxs-lookup"><span data-stu-id="462b5-104">Error code: PRO2614</span></span>

## <a name="symptoms"></a><span data-ttu-id="462b5-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="462b5-105">Symptoms</span></span>

<span data-ttu-id="462b5-106">عند محاولة تأكيد أمر مخطط، تظهر رسالة الخطأ التالية:</span><span class="sxs-lookup"><span data-stu-id="462b5-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="462b5-107">رقم التركيبة المحدد غير معتمَد لأمر دُفعي.</span><span class="sxs-lookup"><span data-stu-id="462b5-107">The selected formula number is not approved for a batch order.</span></span>

## <a name="cause"></a><span data-ttu-id="462b5-108">السبب</span><span class="sxs-lookup"><span data-stu-id="462b5-108">Cause</span></span>

<span data-ttu-id="462b5-109">يقوم النظام بالتحقق من صحة عملية التأكيد لضمان توفر صيغة معتمدة للصنف النشط.</span><span class="sxs-lookup"><span data-stu-id="462b5-109">The system validates the firming operation to make sure that an approved formula is available for the active item.</span></span> <span data-ttu-id="462b5-110">يجب أن توافق على المعادلة على الأرجح.</span><span class="sxs-lookup"><span data-stu-id="462b5-110">You must probably approve the formula.</span></span>

## <a name="resolution"></a><span data-ttu-id="462b5-111">الحل</span><span class="sxs-lookup"><span data-stu-id="462b5-111">Resolution</span></span>

<span data-ttu-id="462b5-112">للموافقة على المعادلة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="462b5-112">To approve a formula, follow these steps.</span></span>

1. <span data-ttu-id="462b5-113">انتقل إلى **إدارة معلومات المنتج \> قوائم مكونات الصنف والمعادلات \> المعادلات**.</span><span class="sxs-lookup"><span data-stu-id="462b5-113">Go to **Product information management \> Bills of materials and formulas \> Formulas**.</span></span>
1. <span data-ttu-id="462b5-114">حدد المعادلة المناسبة.</span><span class="sxs-lookup"><span data-stu-id="462b5-114">Select the relevant formula.</span></span>
1. <span data-ttu-id="462b5-115">في جزء الإجراءات، في علامة تبويب **المعادلة** في مجموعة **الاحتفاظ**، حدد **الموافقة على المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="462b5-115">On the Action Pane, on the **Formula** tab, in the **Maintain** group, select **Approve formula**.</span></span>
1. <span data-ttu-id="462b5-116">في مربع الحوار **الموافقة على قائمة مكونات الصنف**، حدد أحد الموافقين، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="462b5-116">In the **Approve BOM or formula** dialog box, select an approver, and then select **OK**.</span></span>
